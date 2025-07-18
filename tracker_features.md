Feature Customization & Toggle Plan
==================================

| #  | Feature Name                  | Enable/Disable | Customizable Options/Notes                                                                 |
|----|------------------------------|:--------------:|--------------------------------------------------------------------------------------------|
| 1  | Scrape Endpoint              | Yes            | Toggle to enable/disable                                                                  |
| 2  | Announce Rate Limiting       | Yes            | Toggle to enable/disable; make the announce interval/time customizable                    |
| 3  | User/Peer Banning            | Yes            | Option to ban user and/or IP; option to ban only from tracker or site-wide                |
| 4  | Client Whitelisting/Blacklisting | Yes        | Toggle to enable/disable; make whitelist/blacklist configurable                          |
| 5  | Enhanced Peer Expiry         | Yes            | Toggle to enable/disable; make expiry time customizable                                   |
| 6  | Announce Logging & Analytics | Yes            | Toggle to enable/disable logging                                                          |
| 7  | Per-Torrent Access Control   | Yes            | Toggle to enable/disable; if disabled, all torrents are available to everyone             |
| 8  | Bonus/Ratio System           | Yes            | Toggle to enable/disable; make ratio and bonus point rules customizable                   |
| 9  | IPv6/IPv4 Filtering          | Yes            | Toggle to enable/disable                                                                  |
| 10 | Better Error Messages        | Must           | Always enabled                                                                            |
| 11 | Announce Interval Customization | Yes         | Toggle to enable/disable; if disabled, use tracker default interval                       |
| 12 | GeoIP or Country Reporting   | Must           | Always enabled                                                                            |
| 13 | Web UI for Tracker Stats     | Must           | Always enabled                                                                            |
| 14 | Email Notifications          | Yes            | Toggle to enable/disable; uses existing SMTP config                                       |


Tracker Features for Private Trackers
====================================

1. Scrape Endpoint
   - Allows clients to request stats (seeders, leechers, completed) for multiple torrents at once.
   - Useful for tracker statistics and supported by most BitTorrent clients.

2. Announce Rate Limiting
   - Prevents clients from announcing too frequently (e.g., more than once every 30 seconds).
   - Returns a bencoded failure reason if they announce too often, reducing tracker load and abuse.

3. User/Peer Banning
   - Enables admins to ban users or IPs from the tracker.
   - Banned users/peers receive a bencoded failure reason and cannot announce.

4. Client Whitelisting/Blacklisting
   - Only allows certain BitTorrent clients or versions to use the tracker.
   - Blocks known bad or abusive clients, improving network health.

5. Enhanced Peer Expiry
   - Makes peer expiry time configurable.
   - Optionally, expires peers more aggressively if they don’t re-announce, keeping the peer list accurate.

6. Announce Logging & Analytics
   - Logs announce requests for analytics, abuse detection, and debugging.
   - Tracks per-user, per-torrent, and per-IP stats for better management.

7. Per-Torrent Access Control
   - Restricts access to certain torrents (e.g., private, invite-only, or VIP torrents).
   - Only allows users with permission to announce to specific torrents.

8. Bonus/Ratio System
   - Awards bonus points for seeding and enforces minimum ratio requirements for downloading.
   - Encourages healthy sharing and discourages leeching.

9. IPv6/IPv4 Filtering
   - Optionally allows users to filter or prefer IPv4/IPv6 peers.
   - Improves compatibility and privacy for users on different networks.

10. Better Error Messages
    - Returns more descriptive bencoded failure reasons for all error cases (e.g., banned, not authorized, invalid client).
    - Improves user experience and troubleshooting.

11. Announce Interval Customization
    - Dynamically adjusts the announce interval based on tracker load or user status.
    - Helps balance tracker performance and user needs.

12. GeoIP or Country Reporting
    - Optionally includes country or region info for peers (for stats or filtering).
    - Useful for community insights and regional restrictions.

13. Web UI for Tracker Stats
    - Provides a dashboard to view real-time stats, peer lists, and completions.
    - Useful for both users and staff to monitor tracker health.

14. Email Notifications
    - Notifies users of ratio warnings, bans, or important tracker news.
    - Improves communication and community management.