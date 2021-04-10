---
title: Registrierungseinträge zum Nachverfolgen des Installations Fortschritts
description: Registrierungseinträge zum Nachverfolgen des Installations Fortschritts
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player, Nachverfolgen des Installations Fortschritts
- Windows Media Player, Nachverfolgung von Installationsfortschritt
- Windows Media Player, Fortschritt Nachverfolgung von Installationen
- Windows Media Player, Registrierung
- Registrierung, Nachverfolgen des Installations Fortschritts
- Registrierung, Nachverfolgung von Installationsfortschritt
- Registrierung, Fortschritt Nachverfolgung von Installationen
- Registrierung, Einstellungen für Windows-Media Player
- Nachverfolgen des Installations Fortschritts
- Installieren der Statusüberwachung
- fortlaufende Nachverfolgung von Installationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3add1d2feb668ee90418704b9a11b0072530f120
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037594"
---
# <a name="registry-entries-for-tracking-installation-progress"></a><span data-ttu-id="5a9e4-114">Registrierungseinträge zum Nachverfolgen des Installations Fortschritts</span><span class="sxs-lookup"><span data-stu-id="5a9e4-114">Registry Entries for Tracking Installation Progress</span></span>

<span data-ttu-id="5a9e4-115">Mit dem Setup Programm von Windows Media Player 11, Setup \_wm.exe, werden die folgenden Einträge in die Registrierung geschrieben, damit Installationsprogramme den Fortschritt des Windows Media Player Setup-Programms nachverfolgen können, während es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-115">The Windows Media Player 11 setup program, setup\_wm.exe, writes the following entries in the registry so that installation programs can track the progress of the Windows Media Player setup program as it runs.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



<span data-ttu-id="5a9e4-116">In der vorangehenden Registrierungs Syntax ist *value* ein Platzhalter für einen ganzzahligen Wert.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-116">In the preceding registry syntax, *value* is a placeholder for an integer value.</span></span>

<span data-ttu-id="5a9e4-117">Der Fortschritt \_ currentdialog gibt an, welches Dialogfeld Windows Media Player-Setup aktuell angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-117">Progress\_CurrentDialog indicates which dialog box Windows Media Player setup is currently displaying.</span></span> <span data-ttu-id="5a9e4-118">Status \_ maxdialog gibt die Gesamtanzahl der Dialogfelder an, die von Windows Media angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-118">Progress\_MaxDialog indicates the total number of dialog boxes that Windows Media will display.</span></span> <span data-ttu-id="5a9e4-119">Wenn z. b. Progress \_ currentdialog = 2 und Progress \_ maxdialog = 5 angezeigt wird, zeigt Windows Media Player momentan das zweite Dialogfeld in einer Sequenz von fünf an.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-119">For example, if Progress\_CurrentDialog = 2 and Progress\_MaxDialog = 5, Windows Media Player is currently displaying the second dialog box in a sequence of five.</span></span>

<span data-ttu-id="5a9e4-120">Der Fortschritt \_ currentinstall und Progress \_ maxinstall zeigen den Prozentsatz des Abschlusses des aktuellen Dialog Felds an.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-120">Progress\_CurrentInstall and Progress\_MaxInstall, taken together, indicate the percent of completion of the current dialog.</span></span> <span data-ttu-id="5a9e4-121">Wenn z. b. Progress \_ currentinstall = 6 und Progress \_ maxinstall = 25 ist, lautet der aktuelle Dialog 6/25 (24%). ganz.</span><span class="sxs-lookup"><span data-stu-id="5a9e4-121">For example, if Progress\_CurrentInstall = 6 and Progress\_MaxInstall = 25, the current dialog is 6/25 (that is, 24%) complete.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a9e4-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5a9e4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a9e4-123">**Registrierungs Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="5a9e4-123">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




