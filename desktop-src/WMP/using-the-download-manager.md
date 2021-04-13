---
title: Verwenden des Download-Managers
description: Verwenden des Download-Managers
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388760"
---
# <a name="using-the-download-manager"></a><span data-ttu-id="6990b-109">Verwenden des Download-Managers</span><span class="sxs-lookup"><span data-stu-id="6990b-109">Using the Download Manager</span></span>

<span data-ttu-id="6990b-110">Das Windows Media Player SDK enthält eine Beispiel Webseite, die die Verwendung des Download-Managers zum Herunterladen von Dateien auf den Computer des Benutzers veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6990b-110">The Windows Media Player SDK includes a sample webpage that demonstrates using the Download Manager to download files to the user's computer.</span></span> <span data-ttu-id="6990b-111">Sie finden das Beispiel im Ordner mit dem Namen "Webseite", in dem Sie das SDK installiert haben.</span><span class="sxs-lookup"><span data-stu-id="6990b-111">You can locate the sample in the folder named WebPage where you installed the SDK.</span></span> <span data-ttu-id="6990b-112">Der Name der Datei lautet Sample. ASP.</span><span class="sxs-lookup"><span data-stu-id="6990b-112">The name of the file is sample.asp.</span></span> <span data-ttu-id="6990b-113">Das Beispiel bietet die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="6990b-113">The sample provides the following functionality:</span></span>

-   <span data-ttu-id="6990b-114">Erstellt das **Download Manager** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6990b-114">Creates the **DownloadManager** object.</span></span>
-   <span data-ttu-id="6990b-115">Erstellt ein **downloadcollection** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="6990b-115">Creates a **DownloadCollection** object.</span></span>
-   <span data-ttu-id="6990b-116">Startet fünf Dateien herunter, wenn der Benutzer auf **herunterladen** klickt.</span><span class="sxs-lookup"><span data-stu-id="6990b-116">Starts downloading five files when the user clicks **Download**.</span></span> <span data-ttu-id="6990b-117">Im Beispiel werden Standarddatei Pfade bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6990b-117">Default file paths are provided in the sample.</span></span> <span data-ttu-id="6990b-118">Sie sollten diese Standard Pfade durch die Speicherorte von Dateien auf dem eigenen Server ersetzen.</span><span class="sxs-lookup"><span data-stu-id="6990b-118">You should replace these default paths with the locations of files on your own server.</span></span> <span data-ttu-id="6990b-119">Sie können die Pfade ändern, indem Sie die Werte ändern, die dem globalen Array mit dem Namen g \_ sfiles zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="6990b-119">You can change the paths by changing the values assigned to the global array named g\_sFiles.</span></span>
-   <span data-ttu-id="6990b-120">Zeigt Statusinformationen für einen Download an, wenn der Benutzer Sie auswählt.</span><span class="sxs-lookup"><span data-stu-id="6990b-120">Shows status information for a download when the user selects it.</span></span>
-   <span data-ttu-id="6990b-121">Stellt Steuerelemente zum Anhalten, fortsetzen, Abbrechen und Entfernen eines Download Elements bereit.</span><span class="sxs-lookup"><span data-stu-id="6990b-121">Provides controls to pause, resume, cancel, and remove a download item.</span></span>
-   <span data-ttu-id="6990b-122">Verwaltet Informationen zum Herunterladen von Sammlungen zwischen Sitzungen mithilfe von Cookies.</span><span class="sxs-lookup"><span data-stu-id="6990b-122">Maintains information about download collections between sessions by using cookies.</span></span> <span data-ttu-id="6990b-123">Dies ist wichtig, da der Benutzer den Player jederzeit schließen kann.</span><span class="sxs-lookup"><span data-stu-id="6990b-123">This is important because the user can close the Player at any time.</span></span> <span data-ttu-id="6990b-124">Außerdem wird die Online Store-Sitzung beendet, wenn der Benutzer Aufgabenbereiche im Player wechselt.</span><span class="sxs-lookup"><span data-stu-id="6990b-124">Also, if the user switches task panes in the Player, the online store session ends.</span></span>
-   <span data-ttu-id="6990b-125">Verwendet standardmäßig das Herunterladen in Echtzeit.</span><span class="sxs-lookup"><span data-stu-id="6990b-125">Uses real-time downloading by default.</span></span> <span data-ttu-id="6990b-126">Sie können das Verhalten in das Herunterladen im Hintergrund ändern, indem Sie den Wert der Variablen mit dem Namen g \_ SdlType ändern.</span><span class="sxs-lookup"><span data-stu-id="6990b-126">You can change the behavior to background downloading by changing the value of the variable named g\_sDLType.</span></span> <span data-ttu-id="6990b-127">Das Herunterladen im Hintergrund ist für die Verwendung mit dem Betriebssystem Microsoft Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6990b-127">Background downloading is available for use with the Microsoft Windows XP operating system.</span></span>
-   <span data-ttu-id="6990b-128">Synchronisiert die Hintergrundfarbe mit der Farbe des Players.</span><span class="sxs-lookup"><span data-stu-id="6990b-128">Synchronizes the background color with the Player color.</span></span> <span data-ttu-id="6990b-129">Sie können diese Funktion verwenden, um die Darstellung des Online Stores zu ändern, wenn sich der Benutzer entscheidet, die Farbe des Players zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6990b-129">You can use this feature to make your online store change appearance when the user chooses to change the color of the Player.</span></span>

<span data-ttu-id="6990b-130">In den folgenden Abschnitten finden Sie weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="6990b-130">The following sections provide more information:</span></span>

-   [<span data-ttu-id="6990b-131">Die Seite wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="6990b-131">Initializing the Page</span></span>](initializing-the-page.md)
-   [<span data-ttu-id="6990b-132">Starten der Downloads</span><span class="sxs-lookup"><span data-stu-id="6990b-132">Starting the Downloads</span></span>](starting-the-downloads.md)
-   [<span data-ttu-id="6990b-133">Abrufen von Status Informationen</span><span class="sxs-lookup"><span data-stu-id="6990b-133">Retrieving Status Information</span></span>](retrieving-status-information.md)
-   [<span data-ttu-id="6990b-134">Verwalten von Sitzungsinformationen</span><span class="sxs-lookup"><span data-stu-id="6990b-134">Maintaining Session Information</span></span>](maintaining-session-information.md)
-   [<span data-ttu-id="6990b-135">Debuggen der Seite</span><span class="sxs-lookup"><span data-stu-id="6990b-135">Debugging the Page</span></span>](debugging-the-page.md)

## <a name="related-topics"></a><span data-ttu-id="6990b-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6990b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6990b-137">**Programmier Handbuch für den Typ 2-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="6990b-137">**Programming Guide for Type 2 Online Stores**</span></span>](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




