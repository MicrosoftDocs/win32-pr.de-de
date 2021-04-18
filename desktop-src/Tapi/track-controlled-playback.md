---
description: Die folgenden Schritte werden für eine Nachverfolgung gesteuerte Wiedergabe ausgeführt.
ms.assetid: 9069fb32-3978-491b-bb22-f6e736af23d7
title: Track-Controlled Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc657f0d301097edd280c358a34daafa83ef356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358956"
---
# <a name="track-controlled-playback"></a><span data-ttu-id="413b8-103">Track-Controlled Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="413b8-103">Track-Controlled Playback</span></span>

<span data-ttu-id="413b8-104">Gehen Sie folgendermaßen vor, um eine Nachverfolgung gesteuerte Wiedergabe auszuführen:</span><span class="sxs-lookup"><span data-stu-id="413b8-104">To perform track-controlled playback, do the following:</span></span>

-   <span data-ttu-id="413b8-105">Wählen Sie die Option Terminals in Streams nachverfolgen aus.</span><span class="sxs-lookup"><span data-stu-id="413b8-105">Select the Track Terminals onto streams.</span></span>
-   <span data-ttu-id="413b8-106">Erstellen Sie das Terminal Dateiwiedergabe.</span><span class="sxs-lookup"><span data-stu-id="413b8-106">Create the File Playback Terminal.</span></span>
-   <span data-ttu-id="413b8-107">Legen Sie die Eigenschaften – Dateiname und Typ des Speichers fest.</span><span class="sxs-lookup"><span data-stu-id="413b8-107">Set properties—file name and type of storage.</span></span>
-   <span data-ttu-id="413b8-108">Auflisten Sie mithilfe einer Methode im Terminal für die Dateiwiedergabe die dateitrackendterminals.</span><span class="sxs-lookup"><span data-stu-id="413b8-108">Using a method on the File Playback Terminal, enumerate File Track Terminals.</span></span>
-   <span data-ttu-id="413b8-109">Enumerieren von Streams für den TAPI-Befehl.</span><span class="sxs-lookup"><span data-stu-id="413b8-109">Enumerate streams on the TAPI call.</span></span>
-   <span data-ttu-id="413b8-110">Wählen Sie im Stream das dateitrackterminal aus.</span><span class="sxs-lookup"><span data-stu-id="413b8-110">Select the File Track Terminal on the stream.</span></span>
-   <span data-ttu-id="413b8-111">Ruft die [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) -Methode im Terminal der Dateiwiedergabe auf, um die Wiedergabe der aufgezeichneten Daten in den TAPI-Streams zu starten.</span><span class="sxs-lookup"><span data-stu-id="413b8-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of recorded data to the TAPI streams.</span></span>

 

 



