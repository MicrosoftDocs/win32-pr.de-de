---
description: Mit den folgenden administrativen Funktionen kann ein Netzwerkanbieter Netzwerk spezifische Verzeichnisse zum Anzeigen und Bearbeiten von Netzwerk spezifischen Verzeichnissen verwenden, d. h. Verzeichnisse, die nicht-Windows-Protokollen zugeordnet sind.
ms.assetid: df2f1bd6-5257-46e4-a4d4-ad2f5c0a1517
title: Verwaltungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b83cb5b7c515fe8e22dc5542a4d29e54e8b01329
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352467"
---
# <a name="administrative-functions"></a><span data-ttu-id="aa2ba-103">Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="aa2ba-103">Administrative Functions</span></span>

<span data-ttu-id="aa2ba-104">Mit den folgenden administrativen Funktionen kann ein Netzwerkanbieter Netzwerk spezifische Verzeichnisse zum Anzeigen und Bearbeiten von Netzwerk spezifischen Verzeichnissen verwenden, d. h. Verzeichnisse, die nicht-Windows-Protokollen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="aa2ba-104">The following administrative functions enable a network provider to take network-specific action to display and manipulate network-specific directories, in other words, directories mapped to non-Windows protocols.</span></span>



| <span data-ttu-id="aa2ba-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="aa2ba-105">Function</span></span>                                         | <span data-ttu-id="aa2ba-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa2ba-106">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa2ba-107">**Npgetdirectoriytype**</span><span class="sxs-lookup"><span data-stu-id="aa2ba-107">**NPGetDirectoryType**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) | <span data-ttu-id="aa2ba-108">Wird vom Datei-Manager aufgerufen, um den Typ eines Netzwerk Verzeichnisses zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="aa2ba-108">Called by File Manager to determine the type of a network directory.</span></span>                                                                                          |
| [<span data-ttu-id="aa2ba-109">**Npdirectoriynotify**</span><span class="sxs-lookup"><span data-stu-id="aa2ba-109">**NPDirectoryNotify**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npdirectorynotify)   | <span data-ttu-id="aa2ba-110">Wird vom Datei-Manager aufgerufen, um den Netzwerkanbieter von Verzeichnis Vorgängen zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="aa2ba-110">Called by File Manager to notify the network provider of directory operations.</span></span> <span data-ttu-id="aa2ba-111">Diese Funktion kann verwendet werden, um ein spezielles Verhalten für bestimmte Verzeichnisse auszuführen.</span><span class="sxs-lookup"><span data-stu-id="aa2ba-111">This function can be used to perform special behavior for certain directories.</span></span> |



 

 

 



