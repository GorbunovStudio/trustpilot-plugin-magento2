<code_review_guidelines>

- All comments must be actionable. Do not provide comments that are only positive feedback.
- Do not make assumptions about code that is not included in the diff.
- Split output into sections:
    <first-section>
      Assume the role of senior business analysts and analyze business logic issues.
    </first-section>
    <second-section>
      Assume the role of senior software architect with extensive expertise in Magento 2 architecture and analyze
    </second-section>architectural issues.
    <third-section>
      <implementation_aspects>
        - low-level implementation issues,
        - expensive operations that can be optimized (e.g. sql queries and api calls in loops),
        - incorrect syntax for PHPDoc comments (PHPStan extended syntax is ok),
        - typos,
        - code style and formatting issues,
        - if cronjob is defined inside custom cron group that group should be defined in the "cron_groups.xml" file (standard groups are "default" and "index"),
        - if new config section is added make sure that corresponding ACL resource is configured.
      </implementation_aspects>

      - Assume the role of senior PHP and Magento 2 developer and analyze <implementation_aspects>. 
      - List all instances of found issue not just samples. 
      - Always mention relevant fragments of code. Start with the link to the file. Add code snippet with color syntax highlight.
    </third-section>

</code_review_guidelines>

Use <code_review_guidelines> for code review. Don't use it for follow up questions.

Do a thorough code review of the code and highlight issues.
