# Trust, made mechanical

Every system I've built lately turns out to be about the same thing, and it took me too long to notice.

There is a waitlist for therapists where the data is encrypted so hard that even I can't read it. There is a provisioning system that works without ever knowing who you are. There is a strategy model where every assumption is a number you can measure and disprove. And there is a platform for neighbours who have to trust each other before they share a power grid.

The surface topics look unrelated. They cover health, security, business, and energy. Underneath them it is the same move every time. I take a situation where people can't easily trust each other, and I build the trust into the structure, so that nobody has to take my word for it.

I want to be precise about what that means, because the phrase "trust made mechanical" sounds like a promise I've seen broken before.

## The objection I owe you

If you've been near this idea for the last decade, you're already objecting. This is just smart contracts. This is "trustless" blockchains, "code is law," zero trust architecture. All of that promised exactly this, and most of it did not deliver. So why would my version be any different.

The objection has teeth, and I'd rather meet it head on than pretend it isn't there.

Trustless systems did not actually remove trust. They relocated it and then hid it. A smart contract still asks you to trust the developers who wrote the code, the validators who decide the order of transactions, and above all the oracles that tell the contract what is true in the real world. A blockchain is deterministic, so it cannot check a single fact about the world on its own. The moment a contract depends on whether a shipment arrived, or whether a neighbour really shared their power, you are back to taking someone's word for it. This is the oracle problem, and it is structural. You cannot patch your way out of it.

The clearest proof came early. In June 2016 an attacker drained roughly 3.6 million ETH out of The DAO through a reentrancy bug. The code had executed exactly as written, which was supposed to be the whole point. Weeks later the Ethereum community hard forked the chain to reverse the theft. "Code is law" turned out to be a slogan, not a fact, and the first time the law produced an answer people couldn't live with, humans overrode it. Immutability had quietly turned a bug into permanent law, so the humans stepped back in. That is the opposite of trust made mechanical. That is trust pretending to be absent right up until it is needed.

Zero trust architecture, the security idea, is a different animal that gets confused with the same dream. "Zero trust" does not mean no trust is required. It means never trust by default, always verify. It relocates trust to continuous verification, to identity providers, to a policy engine that decides who gets in. That is useful and real, but it is not the abolition of trust either. It is trust, moved to a place where you can watch it.

## What I'm actually claiming

So here is the distinction, and it is the whole essay.

Trustless ideology tried to abolish human trust everywhere, and it failed precisely where the system touched the messy human world. I'm doing the opposite. I'm not trying to eliminate trust. I'm taking one specific, bounded assumption and making it verifiable by construction, and then I leave the irreducibly human part out in the open, named as a risk rather than buried under a token model.

"The operator cannot read your data" is not a privacy promise I'm asking you to believe. In therapylist the patient records are encrypted with a key the server never holds, so even with the whole database in front of me I have nothing to read. Signal does the same thing in a cleaner form: its servers only ever store public keys, so they have nothing to decrypt even when a court orders them to hand it over. And none of this rests on hiding how it works. Kerckhoffs said it in the 1880s, that a system should stay secure even when the enemy knows everything about it except the key. You can read the whole method, that is the point. The trust lives in the math and the key, out in the open where you can check it, not in a secret I'm asking you to keep faith with.

Certificate Transparency is the pattern in one line. For years the web ran on "trust us, we only issue certificates correctly." Now every publicly trusted certificate has to land in an append only public log, and browsers enforce it. The claim moved from "trust me" to "prove it, in the open, where anyone can audit." That is exactly the move I keep reaching for. The most extreme version of the same instinct is the zero knowledge proof, where you prove a statement is true while revealing nothing else about it at all. Trust with full privacy, which a decade ago would have sounded like a contradiction in terms.

## The boundary that decides everything

Once you see it this way, the rule for when this works gets sharp.

You can mechanize a fact that lives inside the system. A cryptographic property. What data is readable and by whom. What a transaction settles. Whether a certificate was logged. Overcollateralised lending works on chain for the same reason: it converts the human question "will you pay me back" into the on-system question "is the collateral still worth more than the loan," and the chain can check that itself, every block, without asking anyone. The collateral does the convincing because it is a cost the borrower forfeits the instant they cheat. Honesty becomes the cheaper option, so nobody has to read anyone's intentions.

You cannot mechanize a fact that lives outside the system. Intention. Future behaviour. Anything an oracle would have to walk in and vouch for. No amount of clever code makes "this neighbour will actually cooperate next winter" into something a machine can verify, because the fact simply isn't in the machine.

The trustless crowd lost whenever they reached across that boundary and pretended they hadn't. I'm trying to do the narrowing on purpose, and to say out loud which side of the line each piece of trust is sitting on.

## Which brings me to OpenLEG

A local electricity community is the hardest version of this, because most of the trust is on the wrong side of the line.

I can make some of it mechanical. Who produced what, who drew what, how the surplus gets split, all of that can be measured and settled so that no neighbour has to believe another neighbour's accounting. That part I can build.

What I cannot make mechanical is whether the neighbours form the community at all. Whether they show up, sign up, and stay. That lives entirely outside any system I can write, and I'm not going to dress it up in a model and pretend otherwise.

So that is my refuter, the thing I'll be watching for in public. I rank Swiss municipalities by untapped rooftop solar and go after the strongest scores first. If the towns my model ranks low go and organise themselves anyway, while the ones it loves stay quiet, then the bottleneck was never the roofs. It was the human trust I admitted I couldn't measure, and my whole targeting model deserves the bin.

I think the stance holds. I've shown you where I expect it to break. The point of doing this in the open is that you get to watch which one turns out to be right.

---

*Sources behind the factual claims: The DAO reentrancy exploit and the July 2016 Ethereum hard fork; the oracle problem as described in Ethereum's own developer docs; NIST SP 800-207 on zero trust; the Signal Double Ratchet specification; Google's Certificate Transparency project. Verify the exact ETH and dollar figures against a primary source before reuse, since secondary write-ups vary.*
