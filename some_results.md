# Some Approximative Testing Results
## Testing 7 Models with 10 Different Commit Messages

### Results by Model:

| Message                        | phi3\:latest | tinyllama\:latest | llama3.2\:latest | gemma3n\:e2b | gemma3:1b | qwen3:0.6b | gemma3n\:latest |
| ------------------------------ | ------------ | ----------------- | ---------------- | ------------ | --------- | ---------- | --------------- |
| Fix authentication bug         | 🔧           | 🎉                | 🛠               | 🔒           | ✅         | —          | 🔒              |
| Add new user dashboard         | 👨           | 👋                | 📈               | 📊           | 👍        | —          | ✨               |
| Update database schema         | 💡           | 🔢                | 💻               | 💾           | 👍        | —          | 💾              |
| Remove deprecated code         | 💥           | 💔                | 🚮               | 🗑           | —         | —          | 🧹              |
| Implement search functionality | 🔍           | 🌊                | 💻               | 🔍           | ✅         | —          | 🔍              |
| Fix memory leak in parser      | 🔧           | 💡                | 🛠               | ✅         | ✅         | —          | 🐛              |
| Add unit tests for API         | 📝           | 💪                | 📝               | 🧪           | ✅         | —          | 🧪              |
| Refactor payment processing    | 💳           | 🎉                | 🛍               | 💳           | ✅         | —          | 💰              |
| Update documentation           | 📚           | 📝                | 📄               | 📝           | 👍        | —          | 📝              |
| Optimize query performance     | 🚀           | 🤑                | ⚡               | 🚀           | 🚀        | —          | 🚀              |

We note here that the qwen3:0.6b is not able to produce emotes properly and
that the tinyllama provides almost random emotes.


### Summary:
- **Total tests performed**: 70 (7 models × 10 messages)
- **Models with major issues**: qwen3:0.6b (consistent unicode issues), tinyllama (incoherent but sort of fun)
- **My top picks**: gemma3n:e4b, llama3.2:3b and phi3:8b
