---
description: Zukünftige Verbesserungen am Winsock-Beispiel Anwendungscode.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Zukünftige Verbesserungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345106"
---
# <a name="future-improvements"></a><span data-ttu-id="47c14-103">Zukünftige Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="47c14-103">Future Improvements</span></span>

<span data-ttu-id="47c14-104">An dieser Anwendung können mehrere Verbesserungen vorgenommen werden, wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="47c14-104">There are several improvements that can be made to this application, such as:</span></span>

-   <span data-ttu-id="47c14-105">Eine einzelne, permanente Verbindung konnte von der Anwendung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="47c14-105">A single, persistent connection could be created by the application.</span></span> <span data-ttu-id="47c14-106">Die entsprechende Fehlerbehandlung muss hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="47c14-106">Appropriate error handling would have to be added.</span></span> <span data-ttu-id="47c14-107">Dadurch wird der Aufwand für das Starten und Löschen der Verbindung reduziert.</span><span class="sxs-lookup"><span data-stu-id="47c14-107">This would reduce the overhead associated with connection startup and teardown.</span></span>
-   <span data-ttu-id="47c14-108">Der Antwort Code auf dem Server kann zum Konsolidieren von Antworten optimiert werden, wodurch die Anzahl der vom Server gesendeten Pakete reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="47c14-108">The reply code on the server could be optimized to consolidate replies, reducing the number of packets sent from the server.</span></span>
-   <span data-ttu-id="47c14-109">Es können Verbesserungen am Protokoll vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="47c14-109">Improvements in the protocol could be made.</span></span> <span data-ttu-id="47c14-110">Beispielsweise könnte eine Update-Bitmaske verwendet werden, um anzugeben, welche Zellen aktualisiert werden sollen, und nur die zu sendenden Zellen Daten.</span><span class="sxs-lookup"><span data-stu-id="47c14-110">For example, an update bitmask could be used to signify which cells are to be updated, and only that cell data sent.</span></span>
-   <span data-ttu-id="47c14-111">Updates können mithilfe verschiedener Threads überlappen, sodass das Netzwerk nicht im Leerlauf ist, während die **computenext** -Funktion ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47c14-111">Updates could be overlapped using different threads, so that the network is not idle while the **ComputeNext** function is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47c14-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47c14-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47c14-113">Verbessern einer langsamen Anwendung</span><span class="sxs-lookup"><span data-stu-id="47c14-113">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="47c14-114">Baselineversion: eine sehr schlechte leistungsfähige Anwendung</span><span class="sxs-lookup"><span data-stu-id="47c14-114">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="47c14-115">Revision 1: Bereinigen der offensichtlichen</span><span class="sxs-lookup"><span data-stu-id="47c14-115">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="47c14-116">Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen</span><span class="sxs-lookup"><span data-stu-id="47c14-116">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="47c14-117">Revision 3: komprimierte Block-Sendevorgang</span><span class="sxs-lookup"><span data-stu-id="47c14-117">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



