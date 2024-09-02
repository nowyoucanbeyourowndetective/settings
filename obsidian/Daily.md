
# 📅 Tasks

<%* 
const yesterday = tp.date.now("YYYY-MM-DD", -1); 
const yesterdayFile = app.vault.getAbstractFileByPath(`Daily Notes/${yesterday}.md`); 
if (yesterdayFile) 
{ 
	const content = await app.vault.read(yesterdayFile); 
	const tasks = content.match(/- \[ \] .*/g); 
	// Matches all incomplete tasks 
	if (tasks) 
	{ 
		tR += tasks.join("\n"); 
	} 
	else { tR += "No incomplete tasks found."; } 
} 
else { tR += "Yesterday's note not found."; } 
%>
- [ ] 
## 🕙 Daily Notes

