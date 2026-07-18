Day 1 — DNS + Arrays & Hashing

What I learned today

Today I started with DNS, the system that translates website names into IP addresses. Basically, DNS works like a phone book for the internet — when you
type google.com into your browser, DNS looks up the actual IP address behind that name so your computer knows where to connect. Without it, we'd have to
memorize a string of numbers for every website instead of just typing a name.

I went through how a DNS lookup actually happens step by step: your browser checks its own cache first, then the OS cache, then it asks a resolver, which
works its way from the root servers down to the TLD servers and finally to the authoritative server that has the real answer. I also learned about
different DNS record types like A, AAAA, CNAME, MX, and TXT, and what a CNAME actually means — it's short for Canonical Name, basically an alias that points
to the real, official name of something. On the security side, I learned why DNS is such a common attack target, through things like DNS spoofing and DNS
hijacking.

After that I moved on to coding practice and worked through two problems from the Arrays and Hashing pattern.

The first one was about checking if any number in an array repeats. I initially thought of comparing every number to every other number, but that
gets slow really fast. Instead I used a hash set to remember numbers I'd already seen, which brought the solution down to linear time.

The second problem added a twist — the duplicate had to appear within a certain distance of index positions, not just anywhere in the array. This
meant a simple hash set wasn't enough anymore since I needed to know exactly where each number appeared. So I switched to a hash map instead, storing each
number along with the last index it showed up at.

The biggest thing I took away from these two problems is a simple way of thinking about when to use which structure. If a problem is just asking
whether something has been seen before, a hash set is enough. But if it's asking where something was seen, or how many times, that's when a hash map
becomes necessary.

Outside of the DNS and coding work, I also spent some time setting up Twingate on my machine to secure remote access to my home network as a
personal project.

Resources I used today
TryHackMe's DNS in Detail room
Neetcode's roadmap to figure out problem order
