# Microsoft-Teams-Integration.
 <!DOCTYPE html>
<html>
<body>
    <h1>Microsoft Integration using Microsoft Graph API</h1>
    <p>This repository contains sample code and instructions on how to integrate with Microsoft Graph API to interact with chat messages and channels in Microsoft Teams.</p>
    <h2>Getting Started</h2>
    <p>These instructions will help you set up and use the integration to retrieve and post messages using Microsoft Graph API.</p>
    <h3>Prerequisites</h3>
    <ul>
        <li>Microsoft Azure Account</li>
        <li>Microsoft Teams Account</li>
        <li>Python 3.x</li>
        <li><code>requests</code> library (Install using <code>pip install requests</code>)</li>
    </ul>
    <h3>Authentication</h3>
    <ol>
        <li>Go to the <a href="https://portal.azure.com/" target="_blank">Azure Portal</a>.</li>
        <li>Create a new App Registration.</li>
        <li>Note down the <strong>Application (client) ID</strong> and create a new client secret.</li>
        <li>Grant necessary permissions (e.g., <code>Chat.Read</code>, <code>ChatMessage.ReadWrite.All</code>) to your app registration.</li>
        <li>Get your tenant ID from the Azure portal.</li>
    </ol>
    <h3>Installation</h3>
    <ol>
        <li>Clone this repository:</li>
    </ol>
    <pre><code>git clone https://github.com/yourusername/microsoft-graph-chat-integration.git
cd microsoft-graph-chat-integration
    </code></pre>
    <ol start="2">
        <li>Create a virtual environment (optional but recommended):</li>
    </ol>
    <pre><code>python3 -m venv venv
source venv/bin/activate  <!-- On Windows: venv\Scripts\activate -->
    </code></pre>
    <ol start="3">
        <li>Install required packages:</li>
    </ol>
    <pre><code>pip install -r requirements.txt
    </code></pre>
    <ol start="4">
        <li>Rename <code>config.sample.json</code> to <code>config.json</code> and fill in your app registration details:</li>
    </ol>
    <pre><code>{
    "client_id": "YOUR_CLIENT_ID",
    "client_secret": "YOUR_CLIENT_SECRET",
    "tenant_id": "YOUR_TENANT_ID"
}
    </code></pre>
    <h2>Usage</h2>
    <ol>
        <li>Run the script to retrieve chat messages:</li>
    </ol>
    <pre><code>python get_chat_messages.py --chat_id "CHAT_ID"
    </code></pre>
    <ol start="2">
        <li>Run the script to post a message to a chat:</li>
    </ol>
    <pre><code>python post_chat_message.py --chat_id "CHAT_ID" --message "Hello from Microsoft Graph API!"
    </code></pre>
    <ol start="3">
        <li>Run the script to post a message to a channel:</li>
    </ol>
    <pre><code>python post_channel_message.py --channel_id "CHANNEL_ID" --message "Hello from Microsoft Graph API!"
    </code></pre>
    <h2>Contributing</h2>
    <p>Feel free to contribute to this project by creating issues or pull requests. Your feedback and contributions are welcome!</p>
    <h2>License</h2>
    <p>This project is licensed under the MIT License - see the <a href="LICENSE">LICENSE</a> file for details.</p>
</body>
</html>
