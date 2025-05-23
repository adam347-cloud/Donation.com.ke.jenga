<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Donations.com - Support Kenyan Causes</title>
    <style>
        /* Base styles */
        body {
            font-family: 'Montserrat', sans-serif; /* Modern font */
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #e0f7fa 0%, #bbdefb 100%); /* Lighter, more vibrant gradient */
            color: #333;
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(90deg, #2196f3 0%, #1976d2 100%); /* Brighter blue gradient */
            color: white;
            padding: 2.5rem 0;
            text-align: center;
            box-shadow: 0 6px 15px rgba(0,0,0,0.2);
            position: sticky;
            top: 0;
            z-index: 50;
        }
        
        .logo {
            font-family: 'Pacifico', cursive; /* More stylistic font for logo */
            font-size: 3rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
        }
        
        .tagline {
            font-size: 1.3rem;
            opacity: 0.95;
            letter-spacing: 1px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        .hero {
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.8) 0%, rgba(255, 87, 34, 0.7) 100%), url('https://images.unsplash.com/photo-1582213782179-e0d53f98f2ca?ixlib=rb-1.2.1&auto=format&fit=crop&w=1600&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 4rem;
            border-radius: 15px;
            text-align: center;
            margin-bottom: 3rem;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle at center, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0) 70%);
            animation: pulse 15s infinite alternate;
        }

        @keyframes pulse {
            0% { transform: scale(1); opacity: 0.1; }
            100% { transform: scale(1.2); opacity: 0.2; }
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
            text-shadow: 2px 2px 6px rgba(0,0,0,0.6);
            font-weight: 700;
        }
        
        .hero p {
            font-size: 1.5rem;
            max-width: 900px;
            margin: 0 auto 3rem;
            line-height: 1.8;
            text-shadow: 1px 1px 4px rgba(0,0,0,0.5);
        }
        
        .donate-btn {
            background-color: #FF5722; /* Vibrant orange */
            color: white;
            border: none;
            padding: 1.2rem 2.8rem;
            font-size: 1.3rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.4s ease;
            box-shadow: 0 6px 20px rgba(255, 87, 34, 0.5);
            text-transform: uppercase;
            font-weight: bold;
            letter-spacing: 1px;
        }
        
        .donate-btn:hover {
            background-color: #E64A19; /* Darker orange */
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 8px 25px rgba(255, 87, 34, 0.7);
        }
        
        .mission {
            display: flex;
            flex-wrap: wrap;
            gap: 2.5rem;
            margin-bottom: 4rem;
        }
        
        .mission-card {
            flex: 1;
            min-width: 300px;
            background: white;
            padding: 2.5rem;
            border-radius: 15px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.1);
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            text-align: center;
        }
        
        .mission-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.15);
        }
        
        .mission-card h2 {
            color: #2196f3; /* Bright blue */
            margin-top: 0;
            font-size: 2rem;
            margin-bottom: 1rem;
        }
        
        .impact {
            background: linear-gradient(rgba(0,0,0,0.75), rgba(0,0,0,0.75)),
                        url('https://images.unsplash.com/photo-1593115057322-e57333d9a93e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1600&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 4rem;
            border-radius: 15px;
            margin-bottom: 3rem;
            text-align: center;
            box-shadow: 0 8px 25px rgba(0,0,0,0.25);
        }
        
        .impact h2 {
            font-size: 2.8rem;
            margin-bottom: 2rem;
            text-shadow: 1px 1px 4px rgba(0,0,0,0.5);
        }
        
        .impact-stats {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 2rem;
        }
        
        .stat {
            background: rgba(255,255,255,0.25);
            padding: 2rem;
            border-radius: 12px;
            min-width: 180px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            backdrop-filter: blur(5px);
            transition: transform 0.3s ease;
        }

        .stat:hover {
            transform: scale(1.05);
        }
        
        .stat-number {
            font-size: 3.2rem;
            font-weight: bold;
            margin-bottom: 0.8rem;
            color: #ffc107; /* Gold color for stats */
            text-shadow: 1px 1px 3px rgba(0,0,0,0.4);
        }
        
        footer {
            background: #1976d2; /* Darker blue */
            color: white;
            text-align: center;
            padding: 2.5rem;
            margin-top: 4rem;
            box-shadow: 0 -4px 15px rgba(0,0,0,0.1);
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 2.5rem;
            margin: 3.5rem 0;
        }
        
        .project-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 8px 25px rgba(0,0,0,0.12);
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            display: flex;
            flex-direction: column;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }
        
        .project-image {
            height: 220px;
            width: 100%;
            object-fit: cover;
        }
        
        .project-info {
            padding: 1.8rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }
        
        .project-info h3 {
            margin-top: 0;
            color: #2196f3; /* Bright blue */
            margin-bottom: 0.8rem;
            font-size: 1.8rem;
        }
        .project-info p {
            font-size: 1rem;
            line-height: 1.7;
            color: #555;
            flex-grow: 1;
            margin-bottom: 1.5rem;
        }
        
        .urgent-tag {
            background: #FF5722; /* Vibrant orange */
            color: white;
            padding: 0.4rem 1rem;
            border-radius: 25px;
            font-size: 0.9rem;
            font-weight: bold;
            display: inline-block;
            margin-bottom: 1rem;
            animation: pulse-urgent 1.5s infinite alternate;
        }

        @keyframes pulse-urgent {
            0% { transform: scale(1); box-shadow: 0 0 0 0 rgba(255,87,34,0.7); }
            100% { transform: scale(1.05); box-shadow: 0 0 0 10px rgba(255,87,34,0); }
        }

        .project-action-buttons {
            display: flex;
            gap: 15px;
            margin-top: auto;
        }

        .project-donate-btn, .project-more-info-btn {
            flex: 1;
            border: none;
            padding: 0.9rem 1.2rem;
            font-size: 1rem;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            font-weight: bold;
            letter-spacing: 0.5px;
        }

        .project-donate-btn {
            background-color: #4CAF50; /* Green */
            color: white;
            box-shadow: 0 4px 10px rgba(76, 175, 80, 0.4);
        }

        .project-donate-btn:hover {
            background-color: #388E3C; /* Darker green */
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(76, 175, 80, 0.6);
        }

        .project-more-info-btn {
            background-color: #607D8B; /* Blue Grey */
            color: white;
            box-shadow: 0 4px 10px rgba(96, 125, 139, 0.4);
        }

        .project-more-info-btn:hover {
            background-color: #455A64; /* Darker Blue Grey */
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(96, 125, 139, 0.6);
        }

        .success-stories, .how-it-helps {
            margin-top: 5rem;
        }

        .section-title {
            text-align: center;
            color: #2196f3; /* Bright blue */
            margin-bottom: 3.5rem;
            font-size: 3rem;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: #FF5722; /* Orange accent */
            margin: 15px auto 0;
            border-radius: 2px;
        }

        .story-grid, .helps-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.5rem;
        }

        .story-card, .help-card {
            background: white;
            padding: 2.5rem;
            border-radius: 15px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.4s ease, box-shadow 0.4s ease;
        }

        .story-card:hover, .help-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.15);
        }

        .story-card img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 1.5rem;
            border: 5px solid #2196f3; /* Blue border */
            box-shadow: 0 0 0 5px rgba(33, 150, 243, 0.3);
        }

        .story-card h4 {
            color: #2196f3;
            margin-bottom: 0.8rem;
            font-size: 1.5rem;
        }

        .help-card h3 {
            color: #2196f3;
            margin-top: 0;
            font-size: 2rem;
            margin-bottom: 1rem;
        }

        /* Comments Section */
        .comments-section {
            margin-top: 5rem;
            padding: 3.5rem;
            background: #fdfdff;
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.08);
        }

        .comments-section h2 {
            color: #2196f3;
            text-align: center;
            margin-bottom: 3rem;
            font-size: 3rem;
        }

        .comment-form {
            background: #ffffff;
            padding: 2.5rem;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.06);
            margin-bottom: 2.5rem;
        }

        .comment-form label {
            display: block;
            margin-bottom: 0.8rem;
            font-weight: bold;
            color: #555;
            font-size: 1.1rem;
        }

        .comment-form input[type="text"],
        .comment-form textarea {
            width: calc(100% - 24px);
            padding: 12px;
            margin-bottom: 1.5rem;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1.05rem;
            transition: border-color 0.3s ease, box-shadow 0.3s ease;
        }

        .comment-form input[type="text"]:focus,
        .comment-form textarea:focus {
            border-color: #2196f3;
            box-shadow: 0 0 0 3px rgba(33, 150, 243, 0.2);
            outline: none;
        }

        .comment-form textarea {
            resize: vertical;
            min-height: 100px;
        }

        .comment-form button {
            background-color: #4CAF50; /* Green */
            color: white;
            border: none;
            padding: 1rem 2rem;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1.1rem;
            transition: background-color 0.3s ease, transform 0.3s ease;
            font-weight: bold;
            letter-spacing: 0.5px;
        }

        .comment-form button:hover {
            background-color: #388E3C; /* Darker green */
            transform: translateY(-2px);
        }

        .comment-list {
            margin-top: 2.5rem;
        }

        .comment-item {
            background: #e3f2fd; /* Light blue background */
            padding: 1.8rem;
            border-radius: 12px;
            margin-bottom: 1.5rem;
            border-left: 6px solid #2196f3; /* Bright blue border */
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
        }
        .comment-item:hover {
            transform: translateX(5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
        }

        .comment-item strong {
            color: #1976d2; /* Darker blue */
            font-size: 1.25rem;
            display: block;
            margin-bottom: 0.5rem;
        }

        .comment-item p {
            margin: 0.5rem 0 0;
            color: #444;
            line-height: 1.7;
        }

        .comment-item small {
            display: block;
            text-align: right;
            color: #777;
            margin-top: 0.8rem;
            font-size: 0.9rem;
        }

        /* Payment Methods Section */
        .payment-methods {
            margin-top: 5rem;
            padding: 3.5rem;
            background: linear-gradient(135deg, #e8f5e9 0%, #c8e6c9 100%); /* Light green gradient */
            border-radius: 15px;
            box-shadow: inset 0 3px 15px rgba(0,0,0,0.08);
            text-align: center;
        }

        .payment-methods h2 {
            color: #2e7d32; /* Darker green for this section title */
            margin-bottom: 3rem;
            font-size: 3rem;
        }

        .payment-methods p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2.5rem;
            color: #4CAF50;
        }

        .payment-options {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 2.5rem;
        }

        .payment-card {
            background: white;
            padding: 2.5rem;
            border-radius: 15px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.1);
            width: 320px; /* Fixed width for consistency */
            text-align: center;
            transition: transform 0.4s ease, box-shadow 0.4s ease;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .payment-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.15);
        }

        .payment-card img {
            max-width: 180px;
            height: auto;
            margin: 0 auto 1.8rem;
            display: block;
        }

        .payment-card h3 {
            color: #2e7d32; /* Darker green */
            margin-bottom: 1.2rem;
            font-size: 1.8rem;
        }

        .payment-card p {
            color: #555;
            margin-bottom: 1.8rem;
            flex-grow: 1; /* Allow paragraph to take space */
            font-size: 1rem;
        }

        .payment-guide-btn {
            background-color: #4CAF50; /* Green */
            color: white;
            border: none;
            padding: 1rem 2rem;
            border-radius: 50px;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.3s ease;
            text-transform: uppercase;
            font-weight: bold;
            letter-spacing: 0.5px;
            box-shadow: 0 4px 10px rgba(76, 175, 80, 0.4);
        }

        .payment-guide-btn:hover {
            background-color: #388E3C; /* Darker green */
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(76, 175, 80, 0.6);
        }

        /* Modal Styles */
        .modal {
            display: none; /* Hidden by default */
            position: fixed; /* Stay in place */
            z-index: 1000; /* Sit on top */
            left: 0;
            top: 0;
            width: 100%; /* Full width */
            height: 100%; /* Full height */
            overflow: auto; /* Enable scroll if needed */
            background-color: rgba(0,0,0,0.7); /* Darker overlay */
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .modal-content {
            background-color: #fefefe;
            padding: 30px;
            border-radius: 15px;
            width: 90%;
            max-width: 900px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.4);
            position: relative;
            animation-name: animatetop;
            animation-duration: 0.5s;
            max-height: 95vh; /* Limit height for scrollability */
            overflow-y: auto; /* Enable scrolling for content */
            transform: scale(0.95); /* Start slightly smaller */
            opacity: 0; /* Start invisible */
        }

        @keyframes animatetop {
            from {top: -300px; opacity: 0; transform: scale(0.8);}
            to {top: 0; opacity: 1; transform: scale(1);}
        }

        .close-button {
            color: #aaa;
            font-size: 32px;
            font-weight: bold;
            position: absolute;
            top: 15px;
            right: 25px;
            cursor: pointer;
            transition: color 0.3s ease;
        }

        .close-button:hover,
        .close-button:focus {
            color: #333;
            text-decoration: none;
            cursor: pointer;
        }

        .modal-body {
            padding: 20px 0;
        }

        .modal-body img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            margin-bottom: 20px;
            display: block;
            margin-left: auto;
            margin-right: auto;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .modal-body h2 {
            color: #2196f3;
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            text-align: center;
        }

        .modal-body h3 {
            color: #4CAF50;
            font-size: 1.8rem;
            margin-top: 2rem;
            margin-bottom: 1rem;
            border-bottom: 2px solid #eee;
            padding-bottom: 5px;
        }

        .modal-body p, .modal-body ul {
            line-height: 1.8;
            margin-bottom: 1rem;
            text-align: justify;
            color: #444;
        }

        .modal-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .modal-gallery img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 10px;
            box-shadow: 0 3px 12px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .modal-gallery img:hover {
            transform: scale(1.08);
            box-shadow: 0 6px 18px rgba(0,0,0,0.15);
        }

        /* Donation Modal Specifics */
        #donationModal .modal-body {
            text-align: center;
        }
        #donationModal .modal-body h2 {
            font-size: 2.8rem;
            color: #FF5722; /* Orange for donation title */
        }
        #donationModal .modal-body p {
            font-size: 1.1rem;
            color: #666;
            margin-bottom: 2rem;
        }

        .donation-form-step {
            display: none; /* Hide steps by default */
            padding: 1.5rem;
            background: #f8f8f8;
            border-radius: 10px;
            margin-top: 1.5rem;
            box-shadow: inset 0 1px 5px rgba(0,0,0,0.05);
            text-align: left;
        }
        .donation-form-step.active {
            display: block;
        }

        .donation-form-step label {
            display: block;
            margin-bottom: 0.8rem;
            font-weight: bold;
            color: #333;
            font-size: 1.05rem;
        }
        .donation-form-step input[type="number"],
        .donation-form-step input[type="text"],
        .donation-form-step select {
            width: calc(100% - 24px);
            padding: 12px;
            margin-bottom: 1.5rem;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
        }
        .donation-form-step input[type="number"]:focus,
        .donation-form-step input[type="text"]:focus,
        .donation-form-step select:focus {
            border-color: #FF5722;
            box-shadow: 0 0 0 3px rgba(255,87,34,0.2);
            outline: none;
        }

        .donation-actions {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 2rem;
        }
        .donation-actions button {
            background-color: #2196f3; /* Blue */
            color: white;
            border: none;
            padding: 0.9rem 1.8rem;
            border-radius: 50px;
            cursor: pointer;
            font-size: 1.1rem;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(33, 150, 243, 0.4);
        }
        .donation-actions button:hover {
            background-color: #1976d2; /* Darker blue */
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(33, 150, 243, 0.6);
        }
        .donation-actions button.back-btn {
            background-color: #607D8B; /* Blue Grey */
        }
        .donation-actions button.back-btn:hover {
            background-color: #455A64;
        }

        .payment-options-modal {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .payment-method-option {
            background-color: #f0f0f0;
            color: #333;
            border: 1px solid #ccc;
            padding: 1rem;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1.1rem;
            font-weight: bold;
            transition: all 0.3s ease;
            text-align: center;
        }

        .payment-method-option:hover {
            background-color: #e0e0e0;
            border-color: #2196f3;
            transform: translateY(-2px);
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        .payment-method-option[data-method="mpesa"]:hover {
            background-color: #c8e6c9; /* Light green */
            border-color: #4CAF50;
        }

        .payment-method-option[data-method="card"]:hover {
            background-color: #e3f2fd; /* Light blue */
            border-color: #2196f3;
        }

        .payment-method-option[data-method="worldremit"]:hover {
            background-color: #ffe0b2; /* Light orange */
            border-color: #FF5722;
        }
        
        .mpesa-guide-content {
            background: #fff3e0; /* Light orange background */
            border: 1px dashed #ffb74d;
            padding: 1.5rem;
            border-radius: 10px;
            margin-top: 1.5rem;
            font-size: 1rem;
            color: #e65100;
            text-align: left;
        }
        .mpesa-guide-content strong {
            color: #d84315;
        }
        .mpesa-guide-content ol {
            list-style-type: decimal;
            padding-left: 20px;
            margin-top: 1rem;
        }
        .mpesa-guide-content li {
            margin-bottom: 0.5rem;
        }

        /* Media Queries for Responsiveness */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 3rem;
            }
            .hero p {
                font-size: 1.3rem;
            }
            .section-title {
                font-size: 2.5rem;
            }
            .mission {
                flex-direction: column;
                gap: 2rem;
            }
        }
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            .hero p {
                font-size: 1.1rem;
            }
            .donate-btn {
                padding: 1rem 2rem;
                font-size: 1.1rem;
            }
            .mission-card {
                min-width: unset;
                flex-basis: 100%;
            }
            .impact-stats {
                flex-direction: column;
            }
            .stat {
                width: 90%;
                margin: 0 auto;
            }
            .projects-grid {
                grid-template-columns: 1fr;
            }
            .story-grid, .helps-grid {
                grid-template-columns: 1fr;
            }
            .payment-card {
                width: 100%;
                max-width: 380px; /* Constrain width for mobile */
            }
            .modal-content {
                width: 95%;
                padding: 20px;
            }
            .close-button {
                font-size: 28px;
                top: 10px;
                right: 15px;
            }
            .modal-body h2 {
                font-size: 2rem;
            }
            .modal-gallery {
                grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            }
            .comments-section, .payment-methods {
                padding: 2rem;
            }
            .payment-method-option {
                padding: 0.8rem;
                font-size: 1rem;
            }
        }

        @media (max-width: 480px) {
            .logo {
                font-size: 2.5rem;
            }
            .tagline {
                font-size: 1rem;
            }
            .hero h1 {
                font-size: 2rem;
            }
            .hero p {
                font-size: 0.95rem;
            }
            .donate-btn {
                padding: 0.8rem 1.5rem;
                font-size: 1rem;
            }
            .section-title {
                font-size: 2rem;
            }
            .project-info h3 {
                font-size: 1.5rem;
            }
            .project-action-buttons {
                flex-direction: column;
                gap: 10px;
            }
            .project-donate-btn, .project-more-info-btn {
                padding: 0.8rem;
                font-size: 0.9rem;
            }
            .comment-form input, .comment-form textarea {
                width: calc(100% - 20px);
                padding: 10px;
            }
            .comment-form button {
                padding: 0.8rem 1.2rem;
                font-size: 0.95rem;
            }
            .payment-guide-btn {
                padding: 0.8rem 1.2rem;
                font-size: 0.95rem;
            }
            .modal-body h2 {
                font-size: 1.8rem;
            }
            .modal-gallery {
                grid-template-columns: repeat(auto-fill, minmax(90px, 1fr));
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">Donations.com</div>
        <p class="tagline">Empowering Kenyan Communities, One Donation at a Time.</p>
    </header>

    <div class="container">
        <section class="hero">
            <h1>Your Support Transforms Lives in Kenya</h1>
            <p>Join us in making a tangible difference. Every shilling contributes to vital projects in education, health, and sustainable development across Kenya.</p>
            <button class="donate-btn" data-project-id="general">Donate Now</button>
        </section>

        <section class="mission">
            <div class="mission-card">
                <h2>Our Mission</h2>
                <p>To connect generous donors with impactful, community-led initiatives in Kenya, ensuring transparency and maximum benefit for those in need.</p>
            </div>
            <div class="mission-card">
                <h2>Our Vision</h2>
                <p>A Kenya where every individual has access to opportunities and resources to thrive, fostering self-reliance and sustainable growth.</p>
            </div>
            <div class="mission-card">
                <h2>Our Values</h2>
                <p>Transparency, Accountability, Community Empowerment, Sustainability, and Compassion are at the heart of everything we do.</p>
            </div>
        </section>

        <section class="impact">
            <h2>Our Impact So Far</h2>
            <div class="impact-stats">
                <div class="stat">
                    <div class="stat-number">KSh 15M+</div>
                    <p>Raised</p>
                </div>
                <div class="stat">
                    <div class="stat-number">50+</div>
                    <p>Projects Funded</p>
                </div>
                <div class="stat">
                    <div class="stat-number">10,000+</div>
                    <p>Lives Impacted</p>
                </div>
                <div class="stat">
                    <div class="stat-number">7</div>
                    <p>Counties Reached</p>
                </div>
            </div>
        </section>

        <h2 class="section-title">Current Projects Needing Your Support</h2>
        <div class="projects-grid">
            <div class="project-card" data-project-id="turkana-classroom">
                <img src="https://images.unsplash.com/photo-1517487856331-50e58832a8ee?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="Children in classroom" class="project-image">
                <div class="project-info">
                    <span class="urgent-tag">Urgent Need</span>
                    <h3>Build a Classroom in Turkana</h3>
                    <p>Many children in Turkana study under trees due to lack of proper infrastructure. Your donation can help us build a safe and conducive learning environment.</p>
                    <div class="project-action-buttons">
                        <button class="project-donate-btn" data-project-id="turkana-classroom" data-suggested-amount="1000">Donate KSh 1,000</button>
                        <button class="project-more-info-btn">More Info</button>
                    </div>
                </div>
            </div>
            <div class="project-card" data-project-id="kisumu-clinic">
                <img src="https://images.unsplash.com/photo-1593115057322-e57333d9a93e?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="Medical outreach" class="project-image">
                <div class="project-info">
                    <h3>Mobile Clinic for Rural Kisumu</h3>
                    <p>Bringing essential healthcare services directly to remote villages in Kisumu, addressing critical health disparities and preventable diseases.</p>
                    <div class="project-action-buttons">
                        <button class="project-donate-btn" data-project-id="kisumu-clinic" data-suggested-amount="500">Donate KSh 500</button>
                        <button class="project-more-info-btn">More Info</button>
                    </div>
                </div>
            </div>
            <div class="project-card" data-project-id="kitui-water">
                <img src="https://images.unsplash.com/photo-1605282583279-b19e9d6d5669?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="Water pump" class="project-image">
                <div class="project-info">
                    <h3>Clean Water Project in Kitui</h3>
                    <p>Providing sustainable access to clean and safe drinking water for thousands in Kitui, reducing waterborne diseases and improving daily life.</p>
                    <div class="project-action-buttons">
                        <button class="project-donate-btn" data-project-id="kitui-water" data-suggested-amount="2500">Donate KSh 2,500</button>
                        <button class="project-more-info-btn">More Info</button>
                    </div>
                </div>
            </div>
            <div class="project-card" data-project-id="nairobi-scholarships">
                <img src="https://images.unsplash.com/photo-1523050854805-4c07d3b078a9?ixlib=rb-1.2.1&auto=format&fit=crop&w=600&q=80" alt="Young student studying" class="project-image">
                <div class="project-info">
                    <h3>Scholarships for Bright Minds (Nairobi Slums)</h3>
                    <p>Empowering bright students from informal settlements in Nairobi to access quality education and break the cycle of poverty.</p>
                    <div class="project-action-buttons">
                        <button class="project-donate-btn" data-project-id="nairobi-scholarships" data-suggested-amount="1500">Donate KSh 1,500</button>
                        <button class="project-more-info-btn">More Info</button>
                    </div>
                </div>
            </div>
        </div>

        <section class="success-stories">
            <h2 class="section-title">Hear From Those You've Helped</h2>
            <div class="story-grid">
                <div class="story-card">
                    <img src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="Mary Wambui" />
                    <h4>Mary Wambui, Nakuru</h4>
                    <p>"Thanks to Donors.com, my child now has access to nutritious meals at school. It's truly changed her life!"</p>
                </div>
                <div class="story-card">
                    <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="David Ochieng" />
                    <h4>David Ochieng, Siaya</h4>
                    <p>"The clean water well means my family no longer walks for hours. It's a miracle for our village."</p>
                </div>
                <div class="story-card">
                    <img src="https://images.unsplash.com/photo-1507003211169-e69adba4c2d9?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="Aisha Omar" />
                    <h4>Aisha Omar, Garissa</h4>
                    <p>"I received a scholarship through this platform. Now I can pursue my dream of becoming a teacher. Asante sana!"</p>
                </div>
            </div>
        </section>

        <section class="how-it-helps">
            <h2 class="section-title">How Your Donation Helps</h2>
            <div class="helps-grid">
                <div class="help-card">
                    <h3>Education</h3>
                    <p>Funding school fees, building classrooms, providing learning materials, and supporting teacher training.</p>
                </div>
                <div class="help-card">
                    <h3>Health</h3>
                    <p>Supporting medical camps, providing essential medicines, improving health facilities, and promoting hygiene.</p>
                </div>
                <div class="help-card">
                    <h3>Livelihoods</h3>
                    <p>Investing in sustainable agriculture, vocational training, and small business grants for economic empowerment.</p>
                </div>
                <div class="help-card">
                    <h3>Water & Sanitation</h3>
                    <p>Drilling boreholes, constructing latrines, and educating communities on proper sanitation practices.</p>
                </div>
            </div>
        </section>

        <section class="comments-section">
            <h2 class="section-title">Share Your Thoughts</h2>
            <div class="comment-form">
                <label for="comment-name">Your Name:</label>
                <input type="text" id="comment-name" placeholder="Enter your name" required>
                <label for="comment-text">Your Comment:</label>
                <textarea id="comment-text" placeholder="Write your comment here..." required></textarea>
                <button type="submit" id="submit-comment">Post Comment</button>
            </div>
            <div class="comment-list" id="comment-list">
                </div>
        </section>

        <section class="payment-methods">
            <h2 class="section-title">How to Donate</h2>
            <p>We offer secure and convenient ways for you to contribute to our impactful projects. Choose the method that works best for you.</p>
            <div class="payment-options">
                <div class="payment-card">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1a/M-PESA_logo.svg/langja-280px-M-PESA_logo.svg.png" alt="M-Pesa Logo">
                    <h3>M-Pesa (For Kenya Residents)</h3>
                    <p>Easily donate via M-Pesa, Kenya's leading mobile money service. Quick, secure, and direct impact.</p>
                    <button class="payment-guide-btn donate-button" data-payment-method="mpesa">Donate via M-Pesa</button>
                </div>
                <div class="payment-card">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1c/WorldRemit_logo.svg/langja-280px-WorldRemit_logo.svg.png" alt="WorldRemit Logo">
                    <h3>WorldRemit (For International Donors)</h3>
                    <p>If you're outside Kenya, you can easily send your donations through WorldRemit. It's fast, secure, and has competitive rates.</p>
                    <button class="payment-guide-btn" id="worldremit-link-btn">Donate via WorldRemit</button>
                </div>
                <div class="payment-card">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/46/Visa_Inc._logo.svg/2560px-Visa_Inc._logo.svg.png" alt="Visa Mastercard Logo">
                    <h3>Credit/Debit Card</h3>
                    <p>A convenient option for both local and international donors using Visa or Mastercard.</p>
                    <button class="payment-guide-btn donate-button" data-payment-method="card">Donate via Card</button>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2025 Donations.com. All rights reserved. Made with ❤️ for Kenya.</p>
    </footer>

    <div id="projectModal" class="modal">
        <div class="modal-content">
            <span class="close-button">&times;</span>
            <div class="modal-body">
                </div>
        </div>
    </div>

    <div id="donationModal" class="modal">
        <div class="modal-content">
            <span class="close-button" id="closeDonationModal">&times;</span>
            <div class="modal-body">
                <h2>Make Your Donation</h2>
                <p id="donationModalIntro">Choose a project and enter your donation details below.</p>

                <div id="step1" class="donation-form-step active">
                    <label for="donation-project">Select Project:</label>
                    <select id="donation-project">
                        <option value="general">General Donation</option>
                        <option value="turkana-classroom">Build a Classroom in Turkana</option>
                        <option value="kisumu-clinic">Mobile Clinic for Rural Kisumu</option>
                        <option value="kitui-water">Clean Water Project in Kitui</option>
                        <option value="nairobi-scholarships">Scholarships for Bright Minds (Nairobi Slums)</option>
                    </select>

                    <label for="donation-amount">Amount (KSh):</label>
                    <input type="number" id="donation-amount" placeholder="e.g., 500, 1000" min="50" required>
                    
                    <label for="donor-name">Your Name:</label>
                    <input type="text" id="donor-name" placeholder="Optional" maxlength="50">

                    <div class="donation-actions">
                        <button id="proceedToPayment">Proceed to Payment</button>
                    </div>
                </div>

                <div id="step2" class="donation-form-step">
                    <h3>Choose Payment Method</h3>
                    <div class="payment-options-modal">
                        <button class="payment-method-option" data-method="mpesa">M-Pesa</button>
                        <button class="payment-method-option" data-method="card">Credit/Debit Card</button>
                        <button class="payment-method-option" data-method="worldremit">WorldRemit (International)</button>
                    </div>
                    <div class="donation-actions">
                        <button class="back-btn" id="backToStep1">Back</button>
                    </div>
                </div>

                <div id="step3-mpesa" class="donation-form-step">
                    <h3>M-Pesa Donation Instructions</h3>
                    <div class="mpesa-guide-content">
                        <h4>How to Donate via M-Pesa:</h4>
                        <ol>
                            <li>Go to your M-Pesa Menu on your phone.</li>
                            <li>Select <strong>Lipa Na M-Pesa</strong>.</li>
                            <li>Select <strong>Pay Bill</strong>.</li>
                            <li>Enter Business No: <strong>[Your Paybill Number Here]</strong> (e.g., <strong>8084000</strong>)</li>
                            <li>Enter Account No: <strong>DONATION</strong> (or the project name if specified, e.g., <strong>TURKANA</strong>)</li>
                            <li>Enter Amount: <strong id="mpesa-amount-display">KSh 0</strong></li>
                            <li>Enter your M-Pesa PIN and Confirm.</li>
                            <li>You will receive an M-Pesa confirmation SMS. Thank you!</li>
                        </ol>
                        <p><strong>Note:</strong> We recommend confirming the exact Paybill and Account Number with our official channels for the most current details.</p>
                    </div>
                    <div class="donation-actions">
                        <button class="back-btn" id="backToStep2Mpesa">Back</button>
                        <button>Done!</button>
                    </div>
                </div>

                <div id="step3-card" class="donation-form-step">
                    <h3>Credit/Debit Card Payment</h3>
                    <p>Our secure online card payment portal is coming soon! In the meantime, please consider using M-Pesa or WorldRemit.</p>
                    <div class="donation-actions">
                        <button class="back-btn" id="backToStep2Card">Back</button>
                    </div>
                </div>

                <div id="step3-worldremit" class="donation-form-step">
                    <h3>WorldRemit Donation Instructions</h3>
                    <p>To donate internationally, please use WorldRemit. We have pre-filled the details for your convenience.</p>
                    <p>Recipient: <strong>Dennis Rotich Ossen</strong></p>
                    <p>M-Pesa Number: <strong>0742884058</strong></p>
                    <div class="donation-actions">
                        <button class="back-btn" id="backToStep2WorldRemit">Back</button>
                        <button id="goToWorldRemitBtn">Go to WorldRemit</button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        const projectModal = document.getElementById('projectModal');
        const closeButton = document.querySelector('#projectModal .close-button');
        const modalBody = document.querySelector('#projectModal .modal-body');

        const donationModal = document.getElementById('donationModal');
        const closeDonationModalButton = document.getElementById('closeDonationModal');
        const donationProjectSelect = document.getElementById('donation-project');
        const donationAmountInput = document.getElementById('donation-amount');
        const donorNameInput = document.getElementById('donor-name');
        const proceedToPaymentButton = document.getElementById('proceedToPayment');
        const mpesaAmountDisplay = document.getElementById('mpesa-amount-display');

        const step1 = document.getElementById('step1');
        const step2 = document.getElementById('step2');
        const step3Mpesa = document.getElementById('step3-mpesa');
        const step3Card = document.getElementById('step3-card');
        const step3WorldRemit = document.getElementById('step3-worldremit');

        const backToStep1Button = document.getElementById('backToStep1');
        const backToStep2MpesaButton = document.getElementById('backToStep2Mpesa');
        const backToStep2CardButton = document.getElementById('backToStep2Card');
        const backToStep2WorldRemitButton = document.getElementById('backToStep2WorldRemit');
        const goToWorldRemitBtn = document.getElementById('goToWorldRemitBtn');

        const commentNameInput = document.getElementById('comment-name');
        const commentTextInput = document.getElementById('comment-text');
        const submitCommentButton = document.getElementById('submit-comment');
        const commentList = document.getElementById('comment-list');

        // Sample comments (for demonstration)
        let comments = [
            { name: "John Doe", text: "Amazing work! Keep changing lives.", timestamp: "2025-05-22 10:30" },
            { name: "Jane Smith", text: "So proud to support these initiatives. Clean water is fundamental.", timestamp: "2025-05-21 15:45" },
            { name: "Local Supporter", text: "Witnessing the impact firsthand. Great transparency!", timestamp: "2025-05-20 09:00" }
        ];

        // Project details data (expanded content for "More Info")
        const projectDetails = {
            "turkana-classroom": {
                title: "Building a Brighter Future: The Turkana Classroom Project",
                content: `
                    <p>In the vast, arid landscapes of Turkana County, education faces immense challenges. Many children, eager to learn, are forced to gather under the scorching sun or seek shelter under sparse trees, their makeshift classrooms offering little protection from the elements or distraction. The lack of proper infrastructure is a significant barrier to quality education, impacting attendance, concentration, and overall learning outcomes.</p>
                    <p>Our "Build a Classroom in Turkana" project aims to address this critical need by constructing durable, well-equipped classrooms that provide a safe, conducive, and inspiring environment for learning. Each classroom will be built using locally sourced, sustainable materials where possible, incorporating designs that maximize natural light and ventilation, crucial for comfort in Turkana's climate.</p>
                    <h3>The Challenge: Education in Arid Lands</h3>
                    <p>Turkana is one of Kenya's largest and most marginalized counties. Decades of underdevelopment, coupled with environmental factors like recurrent droughts, have left its communities vulnerable. Access to education is severely limited by distance, poverty, and a lack of facilities. Children often travel long distances to reach the nearest school, which may be no more than a few poles and a roof, or simply an open space. This significantly contributes to high dropout rates, especially for girls who are often burdened with household chores or early marriages.</p>
                    <p>Beyond the physical structure, a proper classroom symbolizes stability, hope, and the community's commitment to its children's future. It reduces the risk of interruption due to bad weather, provides a dedicated space for learning free from external distractions, and helps foster a sense of importance for schooling among students and parents alike.</p>
                    <h3>Our Solution: A Classroom for Every Child</h3>
                    <p>With your support, we are building permanent, dignified learning spaces. Each classroom will feature:</p>
                    <ul>
                        <li><strong>Durable Walls and Roof:</strong> Protecting students from harsh sun, rain, and dust.</li>
                        <li><strong>Proper Desks and Chairs:</strong> Ensuring ergonomic seating for comfortable learning.</li>
                        <li><strong>Chalkboards/Whiteboards:</strong> Essential tools for interactive teaching.</li>
                        <li><strong>Ventilation and Lighting:</strong> Designed to optimize natural light and airflow, reducing reliance on artificial lighting and keeping temperatures manageable.</li>
                        <li><strong>Integrated Water Harvesting:</strong> Where feasible, rainwater harvesting systems will be installed to provide a local water source for sanitation and drinking, reducing the burden on children to fetch water during school hours.</li>
                        <li><strong>Teacher Accommodations (Optional):</strong> In remote areas, constructing basic teacher housing nearby can attract and retain qualified educators.</li>
                    </ul>
                    <p>The construction process itself also offers benefits, creating temporary employment opportunities for local residents and fostering a sense of community ownership over the new facilities.</p>
                    <h3>Long-Term Impact: Beyond the Walls</h3>
                    <p>The impact of a new classroom extends far beyond its physical walls:</p>
                    <ul>
                        <li><strong>Improved Enrollment and Attendance:</strong> A safe and inviting learning environment encourages more children, especially girls, to attend and stay in school.</li>
                        <li><strong>Enhanced Learning Outcomes:</strong> Conducive conditions lead to better concentration and academic performance.</li>
                        <li><strong>Community Empowerment:</strong> Schools often become central hubs for community activities, adult literacy programs, and health awareness initiatives.</li>
                        <li><strong>Reduced Child Labor:</strong> When children are in school, they are less likely to be engaged in hazardous labor.</li>
                        <li><strong>Breaking the Cycle of Poverty:</strong> Education is a powerful tool for upward mobility, equipping individuals with skills for future employment and self-sufficiency.</li>
                    </ul>
                    <p>We work closely with local community leaders, parents, and educators to identify the areas with the most pressing needs and ensure that the new classrooms serve the community effectively. Every step of the project, from site selection to ribbon-cutting, is a collaborative effort, ensuring sustainability and long-term success.</p>
                    <p>Your contribution, no matter the size, directly translates into bricks, desks, and opportunities for a child in Turkana. Imagine the ripple effect: one child educated can influence their family, their village, and eventually contribute to the development of Kenya as a whole.</p>
                    <p>Join us in laying the foundation for a brighter, more educated future for the children of Turkana. Together, we can build more than just classrooms; we can build dreams.</p>
                `,
                images: [
                    'https://images.unsplash.com/photo-1542810634-71277d0471b0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1582213782179-e0d53f98f2ca?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1517487856331-50e58832a8ee?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1543269871-337c7849c71a?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1516086208-a5905d677610?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1522204523234-87295a702ab9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1552589578-83145452f354?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1579762715104-20a2d216508d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1594157790610-d022b7a9f8e8?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1518173946059-579789311234?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80'
                ]
            },
            "kisumu-clinic": {
                title: "Bringing Healthcare Closer: Mobile Clinic for Rural Kisumu",
                content: `<p>Detailed information about the Mobile Clinic project in Rural Kisumu will go here, including challenges, solutions, and impact. This section would be very long and include many images related to healthcare access, community health workers, and patient stories in rural settings.</p>`,
                images: [
                    'https://images.unsplash.com/photo-1593115057322-e57333d9a93e?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1582719508461-905c67379f06?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1582719478290-bc4f1a27e793?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1598425268482-12f5a6a6f1d9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1582719473672-edc86990d0b0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1582719471384-ce1543260905?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1593115057322-e57333d9a93e?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1582719478290-bc4f1a27e793?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1582719473672-edc86990d0b0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1598425268482-12f5a6a6f1d9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80'
                ]
            },
            "kitui-water": {
                title: "Life-Giving Wells: Clean Water Project in Kitui",
                content: `<p>Detailed information about the Clean Water project in Kitui will go here, including challenges, solutions, and impact. This section would be very long and include many images related to water scarcity, boreholes, community participation, and improved hygiene.</p>`,
                images: [
                    'https://images.unsplash.com/photo-1605282583279-b19e9d6d5669?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1594380724810-7711467406a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1594380724810-7711467406a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1594380724810-7711467406a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1594380724810-7711467406a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1594380724810-7711467406a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1594380724810-7711467406a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1594380724810-7711467406a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1594380724810-7711467406a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1594380724810-7711467406a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80'
                ]
            },
            "nairobi-scholarships": {
                title: "Unlocking Potential: Scholarships for Bright Minds in Nairobi Slums",
                content: `<p>Detailed information about the Scholarships project in Nairobi slums will go here, including challenges, solutions, and impact. This section would be very long and include many images related to student life, graduation, and success stories.</p>`,
                images: [
                    'https://images.unsplash.com/photo-1523050854805-4c07d3b078a9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1523050854805-4c07d3b078a9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1523050854805-4c07d3b078a9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1523050854805-4c07d3b078a9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1523050854805-4c07d3b078a9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1523050854805-4c07d3b078a9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1523050854805-4c07d3b078a9?ixlib=rb-4.2.1&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1523050854805-4c07d3b078a9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1523050854805-4c07d3b078a9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80',
                    'https://images.unsplash.com/photo-1523050854805-4c07d3b078a9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80'
                ]
            }
        };

        // Function to display comments
        function displayComments() {
            commentList.innerHTML = ''; // Clear existing comments
            comments.forEach(comment => {
                const commentDiv = document.createElement('div');
                commentDiv.classList.add('comment-item');
                commentDiv.innerHTML = `
                    <strong>${comment.name}</strong>
                    <p>${comment.text}</p>
                    <small>${comment.timestamp}</small>
                `;
                commentList.appendChild(commentDiv);
            });
        }

        // Add event listener for "More Info" buttons
        document.querySelectorAll('.project-more-info-btn').forEach(button => {
            button.addEventListener('click', function() {
                const projectId = this.closest('.project-card').dataset.projectId;
                const project = projectDetails[projectId];

                if (project) {
                    modalBody.innerHTML = `
                        <h2>${project.title}</h2>
                        ${project.content}
                        <div class="modal-gallery">
                            ${project.images.map(imgSrc => `<img src="${imgSrc}" alt="Project image">`).join('')}
                        </div>
                    `;
                    projectModal.style.display = 'flex'; // Use flex to center the modal
                }
            });
        });

        // Close the project modal
        closeButton.addEventListener('click', function() {
            projectModal.style.display = 'none';
        });

        // Close the modal if clicked outside of the modal-content
        window.addEventListener('click', function(event) {
            if (event.target == projectModal) {
                projectModal.style.display = 'none';
            }
            if (event.target == donationModal) {
                donationModal.style.display = 'none';
                resetDonationModal();
            }
        });

        // Handle comment submission
        submitCommentButton.addEventListener('click', function() {
            const name = commentNameInput.value.trim();
            const text = commentTextInput.value.trim();

            if (name && text) {
                const now = new Date();
                const timestamp = `${now.getFullYear()}-${(now.getMonth() + 1).toString().padStart(2, '0')}-${now.getDate().toString().padStart(2, '0')} ${now.getHours().toString().padStart(2, '0')}:${now.getMinutes().toString().padStart(2, '0')}`;
                comments.unshift({ name, text, timestamp }); // Add new comment to the beginning
                displayComments(); // Re-render comments
                commentNameInput.value = ''; // Clear form
                commentTextInput.value = ''; // Clear form
            } else {
                alert('Please enter both your name and a comment.');
            }
        });

        // Donation Modal Logic
        function showStep(stepElement) {
            document.querySelectorAll('.donation-form-step').forEach(step => {
                step.classList.remove('active');
            });
            stepElement.classList.add('active');
            // Animate the modal content in for a smoother transition
            const modalContent = document.getElementById('donationModal').querySelector('.modal-content');
            modalContent.style.animation = 'animatetop 0.5s';
            modalContent.style.transform = 'scale(1)';
            modalContent.style.opacity = '1';
        }

        function resetDonationModal() {
            showStep(step1);
            donationProjectSelect.value = 'general';
            donationAmountInput.value = '';
            donorNameInput.value = '';
        }

        document.querySelectorAll('.donate-btn, .payment-guide-btn.donate-button, .project-donate-btn').forEach(button => {
            button.addEventListener('click', function() {
                const projectId = this.dataset.projectId || 'general';
                const suggestedAmount = this.dataset.suggestedAmount || '';

                donationProjectSelect.value = projectId;
                donationAmountInput.value = suggestedAmount;
                
                donationModal.style.display = 'flex';
                showStep(step1);
            });
        });

        closeDonationModalButton.addEventListener('click', function() {
            donationModal.style.display = 'none';
            resetDonationModal();
        });

        proceedToPaymentButton.addEventListener('click', function() {
            if (donationAmountInput.value.trim() === '' || parseFloat(donationAmountInput.value) <= 0) {
                alert('Please enter a valid donation amount.');
                return;
            }
            showStep(step2);
        });

        document.querySelectorAll('.payment-method-option').forEach(button => {
            button.addEventListener('click', function() {
                const method = this.dataset.method;
                const donationAmount = donationAmountInput.value;

                if (method === 'mpesa') {
                    mpesaAmountDisplay.textContent = `KSh ${donationAmount}`;
                    showStep(step3Mpesa);
                } else if (method === 'card') {
                    showStep(step3Card);
                } else if (method === 'worldremit') {
                    // WorldRemit handles international payments and often requires a direct link
                    // The step3-worldremit content can be shown to give the user context before linking out
                    showStep(step3WorldRemit);
                }
            });
        });

        // WorldRemit direct link button from within the modal
        goToWorldRemitBtn.addEventListener('click', function() {
            const worldRemitUrl = `https://www.worldremit.com/en/kenya?&recipient_mobile_number=0742884058&recipient_first_name=Dennis&recipient_last_name=Rotich%20Ossen&receive_method=mobile%20money`;
            window.open(worldRemitUrl, '_blank');
            // Optionally, close the modal after redirecting to external site
            donationModal.style.display = 'none'; 
            resetDonationModal();
        });

        // Back buttons
        backToStep1Button.addEventListener('click', () => showStep(step1));
        backToStep2MpesaButton.addEventListener('click', () => showStep(step2));
        backToStep2CardButton.addEventListener('click', () => showStep(step2));
        backToStep2WorldRemitButton.addEventListener('click', () => showStep(step2));

        // Direct WorldRemit link from main page (bottom section)
        document.getElementById('worldremit-link-btn').addEventListener('click', function() {
            const worldRemitUrl = `https://www.worldremit.com/en/kenya?&recipient_mobile_number=0742884058&recipient_first_name=Dennis&recipient_last_name=Rotich%20Ossen&receive_method=mobile%20money`;
            window.open(worldRemitUrl, '_blank');
        });

        // Initial display of comments when the page loads
        displayComments();
    </script>
</body>
</html>
