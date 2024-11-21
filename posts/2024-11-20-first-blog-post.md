Welcome to My First Blog Post: Port Scanners, GitHub, and Sanity… Kinda

Date: November 20, 2024

Hello, World!

Welcome to my very first blog post! If you’re here, you’re probably curious about how a DevOps engineer is morphing into a penetration tester—or maybe you just stumbled in while Googling something about Python scripts. Either way, grab a cup of coffee (or tea, no judgment), and let’s dive into my chaotic yet amusing journey of port scanning, Markdown magic, and figuring out GitHub.

Step 1: GitHub – My Digital Treasure Chest

Let me introduce you to the magic of GitHub. It’s like a treasure chest for nerds—except instead of gold coins, you store Python scripts and notes. I created a repository called Pentest-Tools-and-Notes (creative, I know) to stash all my newfound penetration testing knowledge.

Now, if you’re imagining me typing away furiously, you’re half right. The reality also involved me shouting “Why is this not working?!” at my screen several times. But hey, that’s the price of digital greatness.

Step 2: Writing My First Script – The Digital Speed-Dating for Ports

Ah, the port scanner. The star of today’s show. This little script is like a friendly stalker—it checks whether specific ports on a target machine are open or closed. It’s simple, effective, and doesn’t need any fancy equipment (or restraining orders).

Here’s the Python script I cooked up, complete with a sprinkle of beginner’s luck:

import socket

def port_scanner(target, ports):
    print(f"Starting scan on {target} for {ports} ports...\n")
    for port in range(1, ports + 1):
        sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        result = sock.connect_ex((target, port))
        if result == 0:
            print(f"Port {port}: OPEN")
        else:
            print(f"Port {port}: CLOSED")
        sock.close()

if __name__ == "__main__":
    target = input("Enter target IP: ")
    ports = int(input("Enter number of ports to scan: "))
    port_scanner(target, ports)
    print("\nScan completed.")

The first time I ran this, I felt like a wizard casting a spell. I told it to scan 192.168.0.144 and a few ports, and when Port 80 smiled back at me with a cheerful “OPEN,” I almost applauded. Who needs Netflix when you’ve got Python?	

Step 3: Nmap Cheatsheet – The Pentester’s Best Friend

Nmap is like that multi-tool you keep in your back pocket—it does everything. I wanted to remember all the cool commands I’d found online, so I made a cheatsheet. Here are a few gems:

# Nmap Cheatsheet

## Basic Scans
- Scan a single IP:
  ```bash
  nmap <target-ip>
  
Port Scanning

Scan specific ports:

	nmap -p 80,443 <target-ip>

Save Results

Output results to a file:

	nmap -oN output.txt <target-ip>
	
4. I committed my post to GitHub:

	git add posts/2024-11-20-first-blog-post.md
	git commit -m "Added my first blog post"
	git push origin main
	
Step 5: Lessons Learned

	1. GitHub is my new best friend: It’s like an ultra-organized notebook for all my pentesting tools and notes.
	2. Markdown is a lifesaver: Who knew blogging could be this simple?
	3. Python is pure magic: Writing scripts that actually work on the first try feels like winning the tech lottery.
	4. Humor makes everything better: Whether you’re debugging or blogging, a good laugh can keep you sane.
	
What’s Next?

Next, I’ll dive deeper into penetration testing tools, try not to break my own network (intentionally!), and maybe even scan all the ports on my fridge (because why not?).

If you made it this far, thanks for reading! Stick around for more adventures in tech, laughter, and the occasional Python wizardry.

Stay curious,
WaltQIII
