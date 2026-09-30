# ISBF Views

Counts each signed-in account once per topic when a feed card enters the viewport.
The displayed total combines feed impressions with existing Discourse topic-detail
view records, deduplicated by account. Discourse's own topic view counter remains
independent.

POST /isbf/views/impressions.json accepts topic_ids[] (up to 50) and returns
{ "counts": { "123": 4 } } for topics the current user may view.
