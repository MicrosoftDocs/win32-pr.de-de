---
description: Anwendungen, die die Unicode-und Zeichensatz-API-Funktionen verwenden, verwenden im Allgemeinen dieselbe Fenster Klasse. Das Betriebssystem übersetzt Nachrichten transparent zwischen Fenstern verschiedener Klassen.
ms.assetid: 68e9839b-39f8-411a-8ae4-4a627c667cae
title: Automatische Nachrichten Übersetzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b02a5c5a4951189333608aa448f09ba9c6866d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751168"
---
# <a name="automatic-message-translation"></a><span data-ttu-id="36217-104">Automatische Nachrichten Übersetzung</span><span class="sxs-lookup"><span data-stu-id="36217-104">Automatic Message Translation</span></span>

<span data-ttu-id="36217-105">Anwendungen, die die Unicode-und Zeichensatz-API-Funktionen verwenden, verwenden im Allgemeinen dieselbe Fenster Klasse.</span><span class="sxs-lookup"><span data-stu-id="36217-105">Applications using the Unicode and character set API functions generally use the same window class.</span></span> <span data-ttu-id="36217-106">Das Betriebssystem übersetzt Nachrichten transparent zwischen Fenstern verschiedener Klassen.</span><span class="sxs-lookup"><span data-stu-id="36217-106">The operating system transparently translates messages between windows of different classes.</span></span>

<span data-ttu-id="36217-107">Zum Empfangen von Nachrichten im Unicode-oder Windows-Code Page Format wird eine Fensterfunktion implementiert.</span><span class="sxs-lookup"><span data-stu-id="36217-107">A window function is implemented to receive messages in Unicode or Windows code page format.</span></span> <span data-ttu-id="36217-108">Die Fensterfunktion kann Nachrichten senden oder Funktionen eines beliebigen Typs abrufen.</span><span class="sxs-lookup"><span data-stu-id="36217-108">The window function can send messages or call functions of either type.</span></span>

<span data-ttu-id="36217-109">Die folgenden Meldungen enthalten Textargumente und unterliegen der automatischen Textübersetzung.</span><span class="sxs-lookup"><span data-stu-id="36217-109">The following messages have text arguments and are subject to automatic text translation.</span></span> <span data-ttu-id="36217-110">Informationen zur automatischen Übersetzung finden Sie [unter Unterklassen und automatische Nachrichten Übersetzung](subclassing-and-automatic-message-translation.md).</span><span class="sxs-lookup"><span data-stu-id="36217-110">For information about automatic translation, see [Subclassing and Automatic Message Translation](subclassing-and-automatic-message-translation.md).</span></span>

<dl>

[<span data-ttu-id="36217-111">CB \_ AddString</span><span class="sxs-lookup"><span data-stu-id="36217-111">CB\_ADDSTRING</span></span>](../controls/cb-addstring.md)  
[<span data-ttu-id="36217-112">CB- \_ dir</span><span class="sxs-lookup"><span data-stu-id="36217-112">CB\_DIR</span></span>](../controls/cb-dir.md)  
[<span data-ttu-id="36217-113">CB- \_ FindString</span><span class="sxs-lookup"><span data-stu-id="36217-113">CB\_FINDSTRING</span></span>](../controls/cb-findstring.md)  
[<span data-ttu-id="36217-114">CB \_ getlbtext</span><span class="sxs-lookup"><span data-stu-id="36217-114">CB\_GETLBTEXT</span></span>](../controls/cb-getlbtext.md)  
[<span data-ttu-id="36217-115">CB \_ InsertString</span><span class="sxs-lookup"><span data-stu-id="36217-115">CB\_INSERTSTRING</span></span>](../controls/cb-insertstring.md)  
[<span data-ttu-id="36217-116">CB- \_ SelectString</span><span class="sxs-lookup"><span data-stu-id="36217-116">CB\_SELECTSTRING</span></span>](../controls/cb-selectstring.md)  
[<span data-ttu-id="36217-117">EM \_ getline</span><span class="sxs-lookup"><span data-stu-id="36217-117">EM\_GETLINE</span></span>](../controls/em-getline.md)  
[<span data-ttu-id="36217-118">EM \_ replacesel</span><span class="sxs-lookup"><span data-stu-id="36217-118">EM\_REPLACESEL</span></span>](../controls/em-replacesel.md)  
[<span data-ttu-id="36217-119">EM \_ setpasswordchar</span><span class="sxs-lookup"><span data-stu-id="36217-119">EM\_SETPASSWORDCHAR</span></span>](../controls/em-setpasswordchar.md)  
[<span data-ttu-id="36217-120">LB- \_ AddFile</span><span class="sxs-lookup"><span data-stu-id="36217-120">LB\_ADDFILE</span></span>](../controls/lb-addfile.md)  
[<span data-ttu-id="36217-121">LB- \_ AddString</span><span class="sxs-lookup"><span data-stu-id="36217-121">LB\_ADDSTRING</span></span>](../controls/lb-addstring.md)  
[<span data-ttu-id="36217-122">LB- \_ dir</span><span class="sxs-lookup"><span data-stu-id="36217-122">LB\_DIR</span></span>](../controls/lb-dir.md)  
[<span data-ttu-id="36217-123">LB- \_ FindString</span><span class="sxs-lookup"><span data-stu-id="36217-123">LB\_FINDSTRING</span></span>](../controls/lb-findstring.md)  
[<span data-ttu-id="36217-124">LB- \_ gettext</span><span class="sxs-lookup"><span data-stu-id="36217-124">LB\_GETTEXT</span></span>](../controls/lb-gettext.md)  
[<span data-ttu-id="36217-125">LB- \_ InsertString</span><span class="sxs-lookup"><span data-stu-id="36217-125">LB\_INSERTSTRING</span></span>](../controls/lb-insertstring.md)  
[<span data-ttu-id="36217-126">LB- \_ SelectString</span><span class="sxs-lookup"><span data-stu-id="36217-126">LB\_SELECTSTRING</span></span>](../controls/lb-selectstring.md)  
[<span data-ttu-id="36217-127">WM- \_ askcbformatname</span><span class="sxs-lookup"><span data-stu-id="36217-127">WM\_ASKCBFORMATNAME</span></span>](../dataxchg/wm-askcbformatname.md)  
[<span data-ttu-id="36217-128">WM \_ -Zeichen</span><span class="sxs-lookup"><span data-stu-id="36217-128">WM\_CHAR</span></span>](../inputdev/wm-char.md)  
[<span data-ttu-id="36217-129">WM- \_ Diagramm</span><span class="sxs-lookup"><span data-stu-id="36217-129">WM\_CHARTOITEM</span></span>](../controls/wm-chartoitem.md)  
[<span data-ttu-id="36217-130">WM \_ Erstellen</span><span class="sxs-lookup"><span data-stu-id="36217-130">WM\_CREATE</span></span>](../winmsg/wm-create.md)  
[<span data-ttu-id="36217-131">WM \_ deadchar</span><span class="sxs-lookup"><span data-stu-id="36217-131">WM\_DEADCHAR</span></span>](../inputdev/wm-deadchar.md)  
[<span data-ttu-id="36217-132">WM \_ devmodechange</span><span class="sxs-lookup"><span data-stu-id="36217-132">WM\_DEVMODECHANGE</span></span>](../gdi/wm-devmodechange.md)  
[<span data-ttu-id="36217-133">WM \_ gettext</span><span class="sxs-lookup"><span data-stu-id="36217-133">WM\_GETTEXT</span></span>](../winmsg/wm-gettext.md)  
[<span data-ttu-id="36217-134">WM- \_ mdicreate</span><span class="sxs-lookup"><span data-stu-id="36217-134">WM\_MDICREATE</span></span>](../winmsg/wm-mdicreate.md)  
[<span data-ttu-id="36217-135">WM- \_ menuchar</span><span class="sxs-lookup"><span data-stu-id="36217-135">WM\_MENUCHAR</span></span>](../menurc/wm-menuchar.md)  
[<span data-ttu-id="36217-136">WM- \_ nccreate</span><span class="sxs-lookup"><span data-stu-id="36217-136">WM\_NCCREATE</span></span>](../winmsg/wm-nccreate.md)  
[<span data-ttu-id="36217-137">WM- \_ SetText</span><span class="sxs-lookup"><span data-stu-id="36217-137">WM\_SETTEXT</span></span>](../winmsg/wm-settext.md)  
[<span data-ttu-id="36217-138">WM- \_ syschar</span><span class="sxs-lookup"><span data-stu-id="36217-138">WM\_SYSCHAR</span></span>](../menurc/wm-syschar.md)  
[<span data-ttu-id="36217-139">WM \_ sysdeadchar</span><span class="sxs-lookup"><span data-stu-id="36217-139">WM\_SYSDEADCHAR</span></span>](../inputdev/wm-sysdeadchar.md)  
[<span data-ttu-id="36217-140">WM- \_ wininichange</span><span class="sxs-lookup"><span data-stu-id="36217-140">WM\_WININICHANGE</span></span>](../winmsg/wm-wininichange.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="36217-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36217-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36217-142">Unicode in der Windows-API</span><span class="sxs-lookup"><span data-stu-id="36217-142">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
