---
description: Erfahren Sie, wie Sie das Windows-Explorer-Menüband erweitern.
title: Erweitern der Multifunktionsleiste
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525322"
---
# <a name="extending-the-ribbon"></a><span data-ttu-id="e918b-103">Erweitern der Multifunktionsleiste</span><span class="sxs-lookup"><span data-stu-id="e918b-103">Extending the Ribbon</span></span>

<span data-ttu-id="e918b-104">In Windows-Explorer hilft das Menüband, gängige Aktivitäten für die Dateiverwaltung von Endbenutzern einfacher und leichter auffindbar zu machen, aber es gibt Änderungen für App-Entwickler.</span><span class="sxs-lookup"><span data-stu-id="e918b-104">In Windows Explorer, the Ribbon helps make common end-user file management activities easier and more discoverable, but there are changes afoot for app developers.</span></span> <span data-ttu-id="e918b-105">Die alte Befehlsleiste war z. b. frei erweiterbar, aber das Menüband ist zu diesem Zeitpunkt stärker eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="e918b-105">For example, the old command bar was freely extensible but the Ribbon is more restricted at this time.</span></span> <span data-ttu-id="e918b-106">Außerdem wird das Menüband nicht standardmäßig für alle Namespace Erweiterungen angezeigt, sodass Sie sich für das Menüband entscheiden müssen. Andernfalls erhalten Sie die ältere Befehlsleiste.</span><span class="sxs-lookup"><span data-stu-id="e918b-106">Also, the Ribbon is not shown by default for all namespace extensions, so you have to opt in to get the Ribbon; otherwise, you get the older command bar.</span></span>

<span data-ttu-id="e918b-107">Aktionen, die für Benutzer auf dem Menüband verfügbar sind, können in drei Erweiterbarkeits Kategorien eingeteilt werden:</span><span class="sxs-lookup"><span data-stu-id="e918b-107">Actions available to users on the Ribbon fall into three extensibility categories:</span></span>

-   <span data-ttu-id="e918b-108">Erweiterbarkeit ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e918b-108">Extensibility is not needed.</span></span> <span data-ttu-id="e918b-109">Beispiele: kopieren, einfügen, löschen.</span><span class="sxs-lookup"><span data-stu-id="e918b-109">Examples: Copy, Paste, Delete.</span></span> <span data-ttu-id="e918b-110">Diese Verben werden von Windows verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e918b-110">Windows handles these verbs for you.</span></span>
-   <span data-ttu-id="e918b-111">Die Erweiterbarkeit ist zurzeit nicht zulässig: Beispiele: ZIP, Sitzung schließen und andere benutzerdefinierte Aktionen.</span><span class="sxs-lookup"><span data-stu-id="e918b-111">Extensibility is not currently allowed: Examples: Zip, Close Session, and other custom actions.</span></span> <span data-ttu-id="e918b-112">Verwenden Sie das Kontextmenü, um diese Szenarien abzudecken.</span><span class="sxs-lookup"><span data-stu-id="e918b-112">Use the context menu to cover these scenarios.</span></span>
-   <span data-ttu-id="e918b-113">Die Erweiterbarkeit ist in die Aktion selbst integriert.</span><span class="sxs-lookup"><span data-stu-id="e918b-113">Extensibility is built into the action itself.</span></span> <span data-ttu-id="e918b-114">Beispiele: suchen, e-Mail, drucken, neues Element.</span><span class="sxs-lookup"><span data-stu-id="e918b-114">Examples: Search, Email, Print, New Item.</span></span> <span data-ttu-id="e918b-115">Sie müssen sich für diese Verben registrieren, um Ihre APP oder Ihr Dateiformat in das Menüband einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="e918b-115">You need to register for these verbs to include your app or file format in the Ribbon .</span></span>

<span data-ttu-id="e918b-116">In diesem Dokument wird beschrieben, wie Sie sich für das Menüband anmelden und wie Sie sich registrieren, um bestimmte Menüband-Verben zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="e918b-116">This document describes how you can opt-in to get the Ribbon, and how to register to handle specific Ribbon verbs.</span></span>

## <a name="opting-in-to-the-ribbon"></a><span data-ttu-id="e918b-117">Abonnieren des Menübands</span><span class="sxs-lookup"><span data-stu-id="e918b-117">Opting in to the Ribbon</span></span>

<span data-ttu-id="e918b-118">Um das Menüband zu abonnieren, sollte die [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) -Implementierung das **EP- \_ Menüband** in [**iexplorerpanevisibility:: getpanestate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) angeben und den Wert " **EPS \_ Force** \| **EPS \_ default" \_ auf** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e918b-118">To opt in to the Ribbon, your [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) implementation should specify **EP\_Ribbon** in [**IExplorerPaneVisibility::GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) and return **EPS\_FORCE** \| **EPS\_DEFAULT\_ON**.</span></span>

## <a name="extending-the-ribbon-for-file-extensions"></a><span data-ttu-id="e918b-119">Erweitern des Menübands für Dateierweiterungen</span><span class="sxs-lookup"><span data-stu-id="e918b-119">Extending the Ribbon for File Extensions</span></span>

<span data-ttu-id="e918b-120">Diese Menüband-Schaltflächen sind auf der Grundlage von Dateierweiterungen erweiterbar:</span><span class="sxs-lookup"><span data-stu-id="e918b-120">These Ribbon buttons are extensible based on file extensions:</span></span>

-   <span data-ttu-id="e918b-121">Alle extrahieren</span><span class="sxs-lookup"><span data-stu-id="e918b-121">Extract All</span></span>
-   <span data-ttu-id="e918b-122">\|Einstellungsburn (ein ISO)</span><span class="sxs-lookup"><span data-stu-id="e918b-122">Mount \| Burn (an ISO)</span></span>
-   <span data-ttu-id="e918b-123">Wiedergabe Wiedergabe \| alles \| Hinzufügen zu Wiedergabeliste (Verb: Einreihen in Warteschlange)</span><span class="sxs-lookup"><span data-stu-id="e918b-123">Play \| Play All \| Add to Playlist (verb: Enqueue)</span></span>
-   <span data-ttu-id="e918b-124">Öffnen</span><span class="sxs-lookup"><span data-stu-id="e918b-124">Open</span></span>
-   <span data-ttu-id="e918b-125">Edit (Bearbeiten)</span><span class="sxs-lookup"><span data-stu-id="e918b-125">Edit</span></span>
-   <span data-ttu-id="e918b-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e918b-126">Properties</span></span>

<span data-ttu-id="e918b-127">Wenn Sie sich registrieren, um die relevanten Verben für neue Dateitypen statisch zu behandeln, verarbeitet das Menüband die Verben entsprechend.</span><span class="sxs-lookup"><span data-stu-id="e918b-127">When you register to statically handle the relevant verbs for new file types, the Ribbon handles the verbs appropriately.</span></span> <span data-ttu-id="e918b-128">Sie registrieren sich genauso wie für Kontextmenü Verben.</span><span class="sxs-lookup"><span data-stu-id="e918b-128">You register just as you would for context menu verbs.</span></span> <span data-ttu-id="e918b-129">Weitere Informationen zu Dateizuordnungen und zur Registrierung für Verben finden Sie unter [Verben und Dateizuordnungen](fa-verbs.md) und Erstellen von Kontext [Menü Handlern](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="e918b-129">For more information about file associations and registering for verbs, see [Verbs and File Associations](fa-verbs.md) and [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="registering-as-a-default-handler-for-actionids"></a><span data-ttu-id="e918b-130">Registrieren als Standard Handler für "aktionids"</span><span class="sxs-lookup"><span data-stu-id="e918b-130">Registering as a Default Handler for ActionIds</span></span>

<span data-ttu-id="e918b-131">Registrieren Sie zuerst Ihre ProgID unter dem entsprechenden Unterschlüssel "assocactionid".</span><span class="sxs-lookup"><span data-stu-id="e918b-131">First, register your ProgId under the appropriate AssocActionId subkey.</span></span> <span data-ttu-id="e918b-132">Jeder Unterschlüssel von assocactionid stellt ein Verb oder eine Aktion dar, die Benutzer über das Menüband aufrufen können.</span><span class="sxs-lookup"><span data-stu-id="e918b-132">Each AssocActionId subkey represents a verb or action that users can invoke from the Ribbon.</span></span> <span data-ttu-id="e918b-133">In diesem Beispiel registriert die APP für die zipselection-Aktions-ID, um die Schaltfläche "Alle extrahieren" im Menüband zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="e918b-133">In this example, the app registers for the ZipSelection ActionID to extend the "Extract All" button on the Ribbon.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

<span data-ttu-id="e918b-134">Nachdem diese Registrierung durchgeführt wurde, müssen Sie sich so registrieren, dass Sie die Protokolle wie gewohnt behandelt, wie in [Standardprogramme](default-programs.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e918b-134">Once that registration is complete, you must then register to handle protocols just as you normally would, as described in [Default Programs](default-programs.md).</span></span>

 

 



