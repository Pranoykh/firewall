#  Setup and Use a Firewall on Windows/Linux

**Windows Firewall Configuration**

1. Open Windows Defender Firewall with Advanced Security:

   Search for "Windows Firewall" in the Start Menu and select the option with "Advanced Security.

2. List current rules:

   In the left pane, click on Inbound Rules or Outbound Rules to see the list of active rules.

3. Add a blocking rule:

   * Click New Rule... in the right pane.

   * Select Port and click Next.
   
   * Choose TCP and enter 23 for Telnet in the "Specific local ports" field, then click Next.

   * Select Block the connection and click Next.

   * Choose all network profiles (Domain, Private, Public) and click Next.

   * Name the rule "Block Telnet" and click Finish.

4. Test the rule:

   Open a Command Prompt and try to connect to port 23 using telnet localhost 23.

   The connection should be refused or time out, indicating the rule is working. (Note: You may need to enable the Telnet Client feature in Windows to run this command).

5. Remove the test rule:

   * Find the "Block Telnet" rule in the Inbound Rules list.

   * Right-click the rule and select Delete.

**Summary of Firewall Traffic Filtering**

A firewall acts as a security gatekeeper for your network, inspecting data packets (traffic) entering and leaving your computer. It uses a set of rules to determine whether to allow or deny traffic based on criteria like source/destination IP addresses, port numbers, and protocols (e.g., TCP or UDP).

* Inbound rules control traffic coming into your system.

* Outbound rules control traffic going out of your system.

By default, most firewalls use a "deny-by-default" policy for incoming traffic, meaning all connections are blocked unless there is an explicit rule to allow them. This ensures that only authorized services can communicate with your system, effectively filtering out potential threats.
