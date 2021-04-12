---
title: Erstellen von Disketten mit mehreren Sitzungen
description: Mit IMAPI können Datenträger mit mehreren Sitzungen erstellt werden. Beim Erstellen einer mehr sitzenden CD müssen einige Punkte beachtet werden.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206599"
---
# <a name="creating-discs-with-multiple-sessions"></a><span data-ttu-id="3b2dd-104">Erstellen von Disketten mit mehreren Sitzungen</span><span class="sxs-lookup"><span data-stu-id="3b2dd-104">Creating Discs with Multiple Sessions</span></span>

<span data-ttu-id="3b2dd-105">Mit IMAPI können Datenträger mit mehreren Sitzungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3b2dd-105">IMAPI is capable of creating multi-session data discs.</span></span> <span data-ttu-id="3b2dd-106">Beim Erstellen einer mehr sitzenden CD müssen einige Punkte beachtet werden.</span><span class="sxs-lookup"><span data-stu-id="3b2dd-106">There are a few considerations to be aware of when creating a multi-session disc.</span></span>

<span data-ttu-id="3b2dd-107">Mit der [**idiscmaster:: setactivediscrecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) -Methode wird festgelegt, ob nach der Einstellung eine IMAPI-DVD mit mehreren Sitzungen auf dem aktiven Laufwerk vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3b2dd-107">The [**IDiscMaster::SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) method determines whether there is an IMAPI multi-session disc in the active drive upon setting.</span></span> <span data-ttu-id="3b2dd-108">Wenn dies der Fall ist, wechselt IMAPI automatisch in den multisitzungsmodus.</span><span class="sxs-lookup"><span data-stu-id="3b2dd-108">If so, IMAPI goes into multi-session mode automatically.</span></span> <span data-ttu-id="3b2dd-109">Die Verwendung von [**clearformatcontent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) , nachdem der Modus für mehrere Sitzungen festgelegt wurde, bewirkt, dass IMAPI in den Einzel Sitzungs Modus wechselt.</span><span class="sxs-lookup"><span data-stu-id="3b2dd-109">Using [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) after multi-session mode has been established causes IMAPI to return to single-session mode.</span></span> <span data-ttu-id="3b2dd-110">Dies bedeutet, dass für einen Datensatz mit [**recorddisk**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) ein leeres Laufwerk erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3b2dd-110">This means that a blank disc is required for a [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) burn.</span></span> <span data-ttu-id="3b2dd-111">Wenn sich die Festplatte im Modus für mehrere Sitzungen befindet, muss sich die gleiche Festplatte im aktiven Recorder befinden, oder es wird ein Fehlercode von IMAPI \_ E \_ fehlerdisk zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3b2dd-111">If the disc is in multi-session mode, the same disc must be in the active recorder or an error code of IMAPI\_E\_WRONGDISC will be returned.</span></span>

<span data-ttu-id="3b2dd-112">Die Auswahl einer Aufzeichnung im Joliet-Format bewirkt, dass IMAPI Informationen von der aktuell installierten CD liest. Wenn es sich bei der Festplatte um eine vorherige IMAPI-Joliet-CD handelt, die Platz für eine andere Sitzung hat, legt IMAPI automatisch den Modus für mehrere Sitzungen fest.</span><span class="sxs-lookup"><span data-stu-id="3b2dd-112">Selecting a recorder while in Joliet format causes IMAPI to read information from the currently installed disc. If the disc is a previous IMAPI Joliet disc that has space for another session, IMAPI automatically sets itself to multi-session mode.</span></span> <span data-ttu-id="3b2dd-113">Diese CD muss beim Aufruf von [**recorddisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc)in der aktiven Aufzeichnung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="3b2dd-113">This disc must be present in the active recorder when calling [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span></span>

<span data-ttu-id="3b2dd-114">Das Schließen der ersten Sitzung auf einer CD erfordert 21 MB.</span><span class="sxs-lookup"><span data-stu-id="3b2dd-114">Closing the first session on a disc requires 21 MB.</span></span> <span data-ttu-id="3b2dd-115">Jede zusätzliche Sitzung benötigt 11 MB, um zu schließen.</span><span class="sxs-lookup"><span data-stu-id="3b2dd-115">Each additional session requires 11 MB to close.</span></span>

 

 




