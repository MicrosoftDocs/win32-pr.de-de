---
title: Das Zeichen Fenster
description: Das Zeichen Fenster
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391263"
---
# <a name="the-character-window"></a><span data-ttu-id="71f50-103">Das Zeichen Fenster</span><span class="sxs-lookup"><span data-stu-id="71f50-103">The Character Window</span></span>

<span data-ttu-id="71f50-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="71f50-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="71f50-105">Der Microsoft-Agent zeigt animierte Zeichen in ihren eigenen Fenstern an, die immer am oberen Rand des Fensters z-Reihenfolge angezeigt werden (d. h. immer im Vordergrund).</span><span class="sxs-lookup"><span data-stu-id="71f50-105">Microsoft Agent displays animated characters in their own windows that always appear at the top of the window z-order (that is, always on top).</span></span> <span data-ttu-id="71f50-106">Ein Benutzer kann das Fenster eines Zeichens verschieben, indem er das Zeichen mit der linken Maustaste zieht.</span><span class="sxs-lookup"><span data-stu-id="71f50-106">A user can move a character's window by dragging the character with the left mouse button.</span></span> <span data-ttu-id="71f50-107">Das Zeichen Bild wird mit dem-Zeiger verschoben.</span><span class="sxs-lookup"><span data-stu-id="71f50-107">The character image moves with the pointer.</span></span> <span data-ttu-id="71f50-108">Außerdem kann eine Anwendung mit der [**MoveTo**](moveto-method.md) -Methode ein Zeichen verschieben.</span><span class="sxs-lookup"><span data-stu-id="71f50-108">In addition, an application can move a character using the [**MoveTo**](moveto-method.md) method.</span></span>

<span data-ttu-id="71f50-109">Wenn der Benutzer mit der rechten Maustaste auf ein Zeichen klickt, wird ein Popup Menü angezeigt, in dem die folgenden Befehle angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="71f50-109">When the user right-clicks a character, a pop-up menu appears that displays the following commands:</span></span>

<span data-ttu-id="71f50-110">\|Fenster schließen <span class="underline">V</span>Rach-Befehle Öffnen</span><span class="sxs-lookup"><span data-stu-id="71f50-110">Open \| Close <span class="underline">V</span>oice Commands Window</span></span>

<span data-ttu-id="71f50-111"><span class="underline">H</span>-IDE</span><span class="sxs-lookup"><span data-stu-id="71f50-111"><span class="underline">H</span>ide</span></span>

<span data-ttu-id="71f50-112">----------------------------…</span><span class="sxs-lookup"><span data-stu-id="71f50-112">----------------------------…</span></span>

<span data-ttu-id="71f50-113">Get-Help\*</span><span class="sxs-lookup"><span data-stu-id="71f50-113">Command\*</span></span>


<span data-ttu-id="71f50-114">*Otherhostingapplicationcaption\*\**</span><span class="sxs-lookup"><span data-stu-id="71f50-114">*OtherHostingApplicationCaption\*\**</span></span>

<span data-ttu-id="71f50-115">\*Die aufgeführten Befehle basieren auf dem Eingabe aktiven Client.</span><span class="sxs-lookup"><span data-stu-id="71f50-115">\*Commands listed are based on the input-active client.</span></span> <span data-ttu-id="71f50-116">Weitere Informationen zum Definieren von Befehlen, die im Popup Menü angezeigt werden, finden Sie in der Übersicht über die Microsoft-Agent-Programmierschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="71f50-116">For more information on defining commands that appear in the pop-up menu, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="71f50-117">\*\*Die aufgelisteten Einträge sind alle anderen Anwendungen, die zurzeit das Zeichen sind.</span><span class="sxs-lookup"><span data-stu-id="71f50-117">\*\*Entries listed are all other applications currently hosting the character.</span></span> <span data-ttu-id="71f50-118">Weitere Informationen zum Definieren dieses Eintrags finden Sie in der Übersicht über die Microsoft-Agent-Programmierschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="71f50-118">For more information on defining this entry, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="71f50-119">Mit dem \| Fenster Befehl Schließen Stimmen Befehle öffnen wird die Anzeige des Befehls Fensters des aktuellen aktiven Zeichens gesteuert.</span><span class="sxs-lookup"><span data-stu-id="71f50-119">The Open \| Close Voice Commands Window command controls the display of the Commands Window of the current active character.</span></span> <span data-ttu-id="71f50-120">Wenn sprach Erkennungs Dienste deaktiviert sind, ist dieser Befehl deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="71f50-120">If speech recognition services are disabled, this command is disabled.</span></span> <span data-ttu-id="71f50-121">Wenn sprach Erkennungs Dienste nicht installiert sind, wird dieser Befehl nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="71f50-121">If speech recognition services are not installed, this command does not appear.</span></span>

<span data-ttu-id="71f50-122">Der Hide-Befehl verbirgt das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="71f50-122">The Hide command hides the character.</span></span> <span data-ttu-id="71f50-123">Die Animation, die dem **Versteck** Zustand des Zeichens zugewiesen ist, spielt das Zeichen und blendet es aus.</span><span class="sxs-lookup"><span data-stu-id="71f50-123">The animation assigned to the character's **Hiding** state plays and hides the character.</span></span> <span data-ttu-id="71f50-124">Der Buchstabe "H" in Hide ist die Zugriffstaste des Befehls (mnetmonic).</span><span class="sxs-lookup"><span data-stu-id="71f50-124">The letter "H" in hide is the command's access key (mnemonic).</span></span>

<span data-ttu-id="71f50-125">Die Befehle für die Anwendung (en), die das Zeichen momentan als Host verwenden, folgen dem Hide-Befehl mit vorangestelltem Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="71f50-125">The commands for the application(s) currently hosting the character follow the Hide command, preceded by a separator.</span></span> <span data-ttu-id="71f50-126">Anschließend werden die Namen von anderen Anwendungen, die das Zeichen verwenden, mit einem Trennzeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="71f50-126">Then the names of other applications using the character appear, also preceded by a separator.</span></span>

 

 




