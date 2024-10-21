from flask import Flask, request

app = Flask(__name__)

# Route to get the public IP of the requester
@app.route('/')
def get_public_ip():
    # The 'X-Forwarded-For' header contains the public IP of the requester
    public_ip = request.headers.get('X-Forwarded-For', request.remote_addr)
    return f"Your public IP is: {public_ip}"

if __name__ == '__main__':
    # Run the server on port 5000 and listen on all interfaces
    app.run(debug=True)
