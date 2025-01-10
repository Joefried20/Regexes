# Regexes


select   


'https://example.com',
regexp_extract('https://example.com', r'^[a-z]+') http,
regexp_extract('https://example.com', r'^[a-z]+://') as https,
regexp_extract('https://sub.example.com',r'[a-zA-Z0-9-]+\.[a-zA-Z]+$' ) examplecom,
regexp_extract('https://sub.example.com',r'\.[a-zA-Z]+$') com,
regexp_extract('foo@example.com', r'^([a-zA-Z0-9_.+-]+)@', 1) AS user_name,
  -- regexp_extract('foo@example.com', r'@([a-zA-Z0-9-]+)\.([a-zA-Z0-9-.]+)$', 1) AS domain_name,
REGEXP_EXTRACT('foo@example.com', r'@([a-zA-Z0-9.-]+)$') AS domain_name,
REGEXP_EXTRACT('foo@example.com', r'\.([a-zA-Z0-9]+)$') AS top_level_domain
