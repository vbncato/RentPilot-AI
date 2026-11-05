# ADR-0001: Personal-first product scope

- Status: Accepted
- Date: 2026-11-05
- Decision owners: Founder / Product Owner

## Context
The long-term ambition is a rental assistant that may eventually serve tenants across Europe. Building a public multi-user service immediately would add avoidable product, operational, legal, and architectural complexity before the core value is validated.

## Decision
1. Build the first working version for the Founder's personal rental search in Poland.
2. Use Telegram as the first interface.
3. Design and document the implementation so it can later be made portfolio-ready and prepared for public use, but do not build multi-user SaaS functionality prematurely.
4. A web interface is a later stage, not part of the initial personal MVP unless separately approved.
5. Material architecture decisions must be documented and approved before implementation.

## Consequences
- The initial scope should remain small and useful to one person.
- Reusable boundaries are welcome, but speculative abstractions and premature infrastructure are not.
- Public launch requires a separate review of privacy, security, data-source permissions, attribution, and applicable legal requirements.
