At a high-level, we used lists to represent our routing table. In hindsight, we probably should have used dictionaries for runtime performance and a bit cleaner code. 
Further, in addition to the starter code provided to us, we added had a dictionary field which stored aggregates.
Everytime two routes were aggregated, they were added to this dictionary.
Key: "Network/Netmask:Peer"  ---> Value [List of Base level aggregated routes]

Thus, when we ran into the disaggregate problem, we would take the given route out of the dictionary, then rebuild it using the rest of the base level and repopulating our dictionary. The starter code helped quite a bit in terms of structure / high-level approach. Further, we created a few helper functions like binary_to_ip, get_mask_length, get_masked, etc. which were quite useful for the bit operations needed for masking, unmasking, and aggregating. 

Some challenges we faced were figuring out the source and destination, bit operations, aggregating, and disaggregating. To get through these, sometimes we needed to read through the assignment again, debug our code, look up online as to how bit operations work, as well as thoroughly debugging the disaggregation.

In order to test our code, we ran it against 16 tests provided to us on the Khoury Linux machine. Once things were not working as expected, we would use print statements in order to see how our code was affected our fields / objects. We further imported a pprint library which just formats print statements which would make for easier debugging. In addition, we used git push/pull in order to quickly move code from our local laptops to the Khoury Linux machine. 