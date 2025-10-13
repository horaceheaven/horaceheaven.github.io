---
title: "The Bitter Lesson: Why Computation Beats Human Ingenuity in AI"
collection: publications
type: "Publications"
date: 2025-10-13
permalink: /publications/the-bitter-lesson
---

# The Bitter Lesson: Why Computation Beats Human Ingenuity in AI

In 2019, renowned computer scientist Rich Sutton published what has become one of the most influential essays in artificial intelligence research. His core thesis was deceptively simple yet profoundly challenging: **the biggest lesson from 70 years of AI research is that general methods leveraging computation are ultimately the most effective, and by a large margin**. This principle, known as "The Bitter Lesson," continues to shape how researchers and engineers approach AI development today.[1][2]

## Understanding the Bitter Lesson

The lesson is called "bitter" because it reveals an uncomfortable truth: our human understanding and carefully crafted domain expertise matter far less than we'd like to believe. Time and again throughout AI history, researchers have invested enormous effort encoding human knowledge into their systems only to see these hand-crafted approaches surpassed by simpler methods that leverage raw computational power.[3][1]

Sutton identified a recurring pattern across AI research: researchers initially build knowledge into their agents, which helps in the short term and feels personally satisfying. However, this approach eventually plateaus and even inhibits further progress. Breakthrough advances ultimately come from the opposing approach scaling computation through search and learning.[4]

### The Historical Evidence

Sutton supported his thesis with compelling examples from multiple domains:[2]

**Computer chess** provides the most dramatic illustration. For decades, programmers encoded centuries of chess wisdom into software control the center, develop pieces early, protect the king, and leverage passed pawns. Deep Blue used some chess knowledge combined with brute force search, analyzing 200 million positions per second. But in 2017, AlphaZero achieved something remarkable: it beat world-champion-level players in chess, shogi, and Go with no prior knowledge of these games whatsoever. The system simply trained against itself until it learned optimal strategies.[3]

**Computer vision** followed a similar trajectory. Researchers spent decades designing hand-crafted features like SIFT and HOG based on domain knowledge about how vision should work. These carefully engineered features restricted models to patterns that researchers anticipated. As computation and data scaled, deep networks that learned features directly from pixels decisively outperformed all hand-crafted methods.[5]

**Speech recognition** and **natural language processing** experienced parallel transformations. Systems that relied on linguistic rules and phonetic models gave way to end-to-end neural approaches that learned patterns directly from data.[1]

## Why This Happens

The fundamental driver behind the Bitter Lesson is exponential growth in computational power. Most AI research operates as if computation were constant making human knowledge one of the few ways to improve performance. But over timeframes slightly longer than typical research projects, massively more computation inevitably becomes available.[1]

This creates a strategic tension. Researchers seeking short-term improvements naturally leverage their domain expertise. However, time spent building in human knowledge is time not spent developing methods that scale with computation. The human-knowledge approach tends to complicate systems in ways that make them less suited to leveraging general computational methods.[1]

## Modern Implications and Debates

As of 2025, the Bitter Lesson has become something of biblical text in frontier AI circles, particularly among large language model developers. The explosive success of models like GPT-4 and beyond seems to validate Sutton's thesis massive transformer networks trained on enormous datasets with vast computational resources consistently outperform more specialized approaches.[6][7]

However, new challenges are emerging. While Sutton's original formulation emphasized computation as the primary constraint, recent scaling laws research suggests that **data** may be the new bottleneck. Some researchers now argue for an updated version: "General methods that maximally leverage today's finite data subject to tomorrow's compute limits are ultimately the most effective".[6]

### The Engineering Perspective

The Bitter Lesson has also influenced AI engineering and product development. A pragmatic interpretation suggests adding structure and shortcuts when compute and data are limited, but removing these constraints as resources scale because the shortcuts will eventually bottleneck improvement. This approach acknowledges that different stages of development require different strategies.[5]

## What Makes It Bitter

The lesson stings because it implies that **minds are tremendously, irredeemably complex** far too intricate to be captured by our human intuitions about how intelligence works. Decades of researchers' careful work encoding human expertise proved ultimately less effective than simply throwing more computation at problems.[8][3]

For AI researchers who spent careers building sophisticated knowledge representations, this feels dismissive of their expertise. For those who believe human understanding should guide machine intelligence, it suggests a path toward AI that doesn't reflect how we think we think.[4][1]

Yet embracing this reality has proven key to progress. The researchers and organizations that learned this lesson fastest that computation and data scale trump clever architectural tricks have consistently produced the most capable systems.[9][2]

## Looking Forward

The Bitter Lesson doesn't mean human knowledge is worthless. Rather, it suggests we should focus on building systems that can discover and learn patterns at scale, rather than encoding our assumptions about what those patterns should be. The two general methods that scale arbitrarily with computation search and learning should be our primary tools.[10][1]

As computation continues its exponential growth and AI systems become increasingly capable, Sutton's 2019 essay remains essential reading. Its message is uncomfortable but liberating: **stop trying to make AI think the way we think we think, and instead give systems the computational resources to discover their own solutions**. History suggests that approach will win every time.[9][4][1]

[1](http://www.incompleteideas.net/IncIdeas/BitterLesson.html)
[2](https://www.johndcook.com/blog/2025/02/20/bitter-lesson/)
[3](https://www.oneusefulthing.org/p/the-bitter-lesson-versus-the-garbage)
[4](https://corinwagen.github.io/public/blog/20231201_sutton.html)
[5](http://rlancemartin.github.io/2025/07/30/bitter_lesson/)
[6](https://obviouslywrong.substack.com/p/the-bitter-lesson-is-misunderstood)
[7](https://www.linkedin.com/posts/andrew-trask-3763ba15b_ive-just-drafted-a-new-blogpost-the-bitter-activity-7378134311562129409-uzVi)
[8](https://www.reddit.com/r/MachineLearning/comments/b179cs/d_the_bitter_lesson/)
[9](https://leonwu.tech/posts/bitter-lesson)
[10](https://www.youtube.com/watch?v=MPWtR--nU0k)
[11](https://www.cs.utexas.edu/~eunsol/courses/data/bitter_lesson.pdf)
[12](https://arxiv.org/html/2410.09649v1)
[13](https://www.reddit.com/r/agi/comments/194xy22/the_bitter_lesson_the_biggest_lesson_that_can_be/)
[14](https://nat.io/blog/bitter-lesson-revisited)
[15](https://www.beren.io/2020-07-13-Reflections-On-The-Bitter-Lesson/)
[16](https://aclanthology.org/2024.nlp4science-1.15/)
[17](https://www.dbreunig.com/2025/08/01/does-the-bitter-lesson-have-limits.html)
[18](https://x.com/richardssutton?lang=en)
[19](https://hex.tech/blog/bitter-lessons-building-ai-in-hex-product-management/)
[20](https://lukaspetersson.github.io/blog/2025/bitter-vertical/)