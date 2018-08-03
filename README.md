# APM-Multi-DC-Persistence
APM Multiple Datacenter Persistence iRule

credit to Rossel Vermette

Issue we are trying to resolve:
A client comes into a VS (LTM/APM enabled) in one datacenter, and in “mid session”, the client does a dns lookup which resolves to some other DataCenter.  (example,  mobile devices, or certain carriers use anycast dns, or proxies the DNS traffic where GTM won’t be able to keep persistency, but because the dns query comes from a different “client local dns servers”, they can get sent to a different DC and GTM persistency will not work.) 
