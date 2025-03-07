# Summary of IPv6 PDF

## **Introduction to IPv6**

-   **IPv6**  provides a significantly larger address space compared to IPv4.
    
    -   **IPv4**: 32-bit addressing (~4.3 billion addresses).
        
    -   **IPv6**: 128-bit addressing (~340 undecillion addresses).
        

## **Why IPv6 is Needed**

-   **Growth of the Internet**: Increasing number of connected devices (IoT).
    
-   **IPv4 Address Depletion**: Limited IPv4 addresses are running out.
    
-   **Modern Technologies**: Better support for current and future technologies.
    

## **Advantages of IPv6 over IPv4**

1.  **Larger Address Space**: Every device can have a unique address.
    
2.  **Eliminates NAT**: No need for Network Address Translation, improving network speed.
    
3.  **No Broadcasts**: Replaced by multicasts, reducing bandwidth usage.
    
4.  **Simplified Header**: More efficient packet processing.
    
5.  **Efficient Routing**: Hierarchical design reduces routing table size.
    
6.  **Enhanced Security**: Built-in security features.
    
7.  **Auto-Configuration (SLAAC)**: Simplifies network administration, ideal for IoT.
    

## **IPv6 Addressing**

-   **Address Format**:
    
    -   **Hexadecimal notation**: Groups of four 16-bit numbers (hextets) separated by colons.
        
    -   **Compression**: Leading zeros and consecutive zeroes can be omitted.
        
    -   **Examples**:
        
        -   Full:  `2001:0db8:0001:0000:0000:0ab9:C0A8:0102`
            
        -   Compressed:  `2001:db8:1::ab9:C0A8:102`
            
-   **Address Types**:
    
    -   **Unicast**: One-to-one communication.
        
    -   **Multicast**: One-to-many communication.
        
    -   **Anycast**: One-to-closest communication.
        
-   **Routable vs. Non-Routable Addresses**:
    
    -   **Non-Routable**: Link-local addresses (e.g.,  `FE80::/10`), used within a local network.
        
    -   **Routable**: Global unicast addresses (e.g.,  `2000::/3`), used on the public Internet.
        

## **IPv6 Header Format**

-   **Simplified Header**: Compared to IPv4, IPv6 has a more streamlined header.
    
-   **Key Fields**:
    
    -   **Version**: Specifies IPv6.
        
    -   **Priority (Traffic Class)**: Identifies traffic type for congestion control.
        
    -   **Flow Label**: Identifies a group of packets for Quality of Service (QoS).
        
    -   **Payload Length**: Length of the IP datagram excluding the header.
        
    -   **Next Header**: Defines the next header or upper-layer protocol.
        
    -   **Hop Limit**: Replaces IPv4's TTL (Time to Live).
        

## **Extension Headers**

-   IPv6 allows up to six extension headers for additional functionality:
    
    -   **Hop-by-Hop Options**: Special management or debugging.
        
    -   **Source Routing**: Defines routing path.
        
    -   **Fragmentation**: Only the source can fragment packets.
        
    -   **Authentication**: Validates sender and data integrity.
        
    -   **Encrypted Security Payload**: Provides confidentiality.
        
    -   **Destination Options**: Information for the destination only.
        

## **Neighbor Discovery Protocol (NDP)**

-   **Replaces ARP**: Used for discovering and communicating with devices on the same network.
    
-   **Key Messages**:
    
    -   **Neighbor Solicitation (NS)**: Requests a neighbor's MAC address.
        
    -   **Neighbor Advertisement (NA)**: Provides the requested MAC address.
        
    -   **Router Solicitation (RS)**: Requests router advertisements.
        
    -   **Router Advertisement (RA)**: Advertises router presence and network prefix.
        

## **Stateless Address Autoconfiguration (SLAAC)**

-   **Automatic Configuration**: Devices configure their own IP addresses without DHCP.
    
-   **Process**: Routers send RA messages with network prefixes, and devices combine this with their Interface Identifier to form an IPv6 address.
    
-   **Benefits**:
    
    -   **Ease of Use**: No manual configuration or DHCP server needed.
        
    -   **Scalability**: Ideal for large networks.
        
    -   **Reduced Management Overhead**: No need for DHCP server management.
        
-   **Limitations**: Only for basic configuration; DHCPv6 may still be needed for complex setups.
    

## **IPSec in IPv6**

-   **IPSec**: A suite of protocols for securing IP communications.
    
-   **Mandatory in IPv6**: Unlike IPv4, where it is optional.
    
-   **Key Features**:
    
    -   **Confidentiality**: Encrypts data.
        
    -   **Integrity**: Ensures data hasn’t been altered.
        
    -   **Authentication**: Verifies the identity of communicating parties.
        
    -   **Anti-Replay Protection**: Prevents malicious reuse of packets.
