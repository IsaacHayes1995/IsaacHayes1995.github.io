---
pubDate: 2025-02-02
author: "Isaac Hayes"
title: "The Swiss Cheese Receive"
description: "How to increase your soiled-in RFID accuracy"
authorAvatar:
  url: "/images/authors/linen-hub.jpg"
  alt: "image alt"
image:
  url: "/reflections/swiss-cheese-receiving.webp"
  alt: "#_"
tags: ["rfid", "soiled-in", "accuracy"]
---
# The Importance of 'Soiled In' Scanning

Every laundry that has implemented, or attempted to implement RFID at some level, has had issues with accuracy.
The sheer volume of items that pass through a laundry seems to suggest that 100% accuracy is impossible.

But when attempting to track linen using RFID, the soiled in scanning is hand-down the most important aspect.
Missed reads when shipping items to a customer, whilst a problem, impacts the data in a very different way to a missed read receiving linen.

---

## Example Scenario: Obie’s Linen Services

For illustration purposes, let’s use our fictional laundry: ‘Obie’s Linen Services’, who is servicing the customer ‘Alice’s Restaurant’.
Obie’s Linen is using RFID to track how much linen is on site at Alice’s Restaurant.

On Monday 100 tablecloths are sent to Alice’s Restaurant, and this trolley of table-linen 
is put through the trolley scanner, but only 98 are scanned!
How does this mismatch affect both the customer and the laundry?

### What’s the impact?
Well if we look at an aged linen report, we would see that our RFID system considers 98 items to be on site.
In reality there are 100, but these 2 freebies aren’t accounted for.


#### From the laundry’s perspective:
- It creates uncertainty: are the missing two lost?

#### From Alice’s perspective:
- No issue! They're not accountable for those two sheets.


From the laundries perspective it causes an issue, because we can’t know if these two items were lost.
But from Alice’s perspective, it’s no skin off her  nose, because they just aren’t being held accountable for those 2 sheets!

---

### Let’s Go Extreme
Now for the sake of illustration, let’s say Alice’s Restaurant takes that trolley of 100 sheets pushes it to the bottom of a cliff.

At the end of the month Obie meets with Alice, to discuss their linen usage:

> “I can see here that you never returned 98 sheets to us, do you have them on site?”

> “Seems not, Obie, let’s settle up.”

The laundry is able to confidentially account for 98 sheets, and can fairly charge for the loss.


---

## Now Flip It: Inaccuracy on the Soiled-In Side
Now what if our inaccuracy is at the ‘soiled in’ side?
Obie’s laundry sends 50 serviettes to Alice’s Restaurant, and scans them out. All 50 scan correctly. 

After a large function, Alice sends all 50 back, however only 48 of them are scanned back.
The end of the month rolls around and Obie and Alice sit down to discuss the linen movements.

At the end of the month:

> “Looks like we never got back 2 serviettes!”  

> “We definitely sent them all back...”


And therein lies the issue with inaccurate soiled reads:
It creates false positives, whereas inaccurate shipping scanning creates false negatives.

False negatives are silent, and can become a problem to the laundry if left unchecked, however a false positive (linen not scanned back from the customer) creates a situation where the laundry believes linen is still at the customer, and can create conflict, or worse erroneous charges to the customer. 

---

# The Swiss Cheese Receive
So now that we know that accuracy in our soiled in scanning should be our top priority, how do we achieve this?
Well we look to our swiss dairy products for guidance.

In risk analysis, the “Swiss Cheese Model” shows how holes (failures) in multiple layers can align.
However as you add more layers, the probability that holes would align in *all* the layers is greatly reduced.

If we take this approach to our soiled in scanning, our ‘holes’ in the slices are missed reads. 
Multiple read points in the process whose accuracy is well below 100%, 
can very quickly add up to a percentage very close to it.

## The Example
Let’s first imagine this set up:

A single conveyor, where all soiled linen passes through to the sorting deck.
On this conveyor is a single rfid reader, and it reads 95% of all tags that pass it.

What is our total accuracy in this scenario?
It’s not a trick question, it’s 95%.

That means that for every one million items that pass through the laundry, fifty thousand items are missed.
Would you be confident talking to customers about their lost linen with those sorts of numbers? I certainly wouldn’t.

Now what happens if put another reader on CBW chute conveyor. This reader also captures 95% of all linen that passes it. Unfortunately it doesn’t know which items were missed at the first reader, since it’s not sentient and can’t know things, so it just captures 95% of all linen it sees.
Now what is our total accuracy?

Either of these readers individually gives us 95% accuracy, but how do we calculate our total accuracy with them together?
Well let’s look at a single sheet, and the probability that it will be missed and work from there.
With our first reader on its lonesome, the probability that any one sheet would be missed is 5%, or 0.05. Pretty simple stuff.
From there to calculate probability of two independent events occuring together, we simple multiply them. If I flip a coin once, the probability of it landing on heads is 50%, or 0.5. If I flip a coin twice, the probability of it landing on heads both times is 0.5 * 0.5 = 0.25 or 25%.
So back to our two reader example, if the probability of our single sheet being missed on the first reader is 0.05 (5%) and the probability of it being missed on the second reader is also 0.05, then the probability of it being missed on both readers is 0.05 * 0.05 = 0.0025 (0.25%), or a quarter of a percent!
That means we’ve brought our accuracy to 99.9975%!

Now that looks like a pretty flash number, that Obie might be proud to share, but let’s go back to our million items example.
For every million items that pass through the laundry, at 99.9975% accuracy, we are still missing 2,500 items! This level of accuracy might be okay in some cases, but if we are going to use this data as the basis of some hard conversations, we can’t be sure that those 2,500 items aren’t the ones we are asking for our customer to pay for.
So let’s add another point of reading. This time we put a reader behind the dryers on a conveyor, and this one only captures 90% of items.
Where are we at now with our total accuracy?
0.05 * 0.05 * 0.1 = 0.00025 chance of one sheet being missed, or 99.99975% (we’ve added another nine after the denominator),
So now for every million, we are missing only 250 sheets! That’s right, our lousy 90% accurate reader has made a big difference in our overall accuracy.
Still not happy with a whole 250 sheets being missed per million, but not prepared to spend any more money on readers, Obie goes to his RFID software provider and confirms that anything he ships out the door will be counted as a “soil in” if it w hadn’t been previously picked up.

His dispatch cabinet is now acting as the last line of defence in his Swiss Cheese Receive model. His dispatch cabinet captures 98% of linen that goes through it, and we will ignore variables such as damaged linen that never makes back out the door (assuming these will be scanned manually when discarded). So that gives us another 98% accurate reader to tack on to our system.
0.05 * 0.05 * 0.1 * 0.02 = 0.000005 chance of a single sheet being missed.
That’s 99.999995% accurate, or, as in our million sheets example, 5 sheets missed per million. A much more manageable number, and one that can be waived in advance to the customer, essentially offering them this amount of lost linen at no fee, to ensure they aren’t left holding the bag for the laundries inaccuracies.
Now comes your question: that’s all well and good Isaac, but how do I proved that we are this accurate to my customer?
That’s a brilliant question and I wish I had thought of it myself, here’s your answer:

# Audit, Audit, Audit
It’s not enough to tell your customer that your soiled in process is accurate, you need to prove it to them. And the only way to prove that your soiled in process is accurate, either to yourself or to your customer, is to audit it.
Auditing does need to be a part of the particular RFID software you use, it is predominantly an operational process, rather than a technological one.
The auditing process is simple: You have pretend customer on site. You ship linen to the pretend customer. Then you return it. Take the linen and send it back to the washroom to be processed as normal. You can verify with certainty that you sent all the linen back, so what does your RFID report look like for that customer?

If things are going well with your system, you should see 100% of that linen taken off their account. You log this, and then rinse and repeat every day.

This does two things: first it quickly alerts you to an issue, should the audit show a low return percentage. The second is it gives you something tangible you can show your customers.
“How do I know you didn’t miss these items when I returned them?”
“Here is the last 6 months of daily audits we performed, showing the accuracy of our soiled in process”
Is a lot smoother than:
“How do I know you didn’t miss these items when I returned them?”
“Trust me, bro.”
With the swiss cheese receive, and regular audits, you can assure your customer, and yourself for that matter, that your RFID process is tight, and nothing is falling through the cracks. Trust in the system is paramount if you wish to extract real value from your RFID infrastructure.

