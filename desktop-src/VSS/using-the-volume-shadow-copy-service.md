---
description: Bei VSS-Sicherungs-und-Wiederherstellungs Vorgängen wird jeweils ein Protokoll für die Interaktion der Systeme verwendet, die Massenspeicher (Writer) verwenden, und diejenigen, die Sie sichern (Requester).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Verwenden des Volumeschattenkopie-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a1c81d79de30085f783feb02b7a7d47d5dc765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526303"
---
# <a name="using-the-volume-shadow-copy-service"></a><span data-ttu-id="8ba9a-103">Verwenden des Volumeschattenkopie-Dienst</span><span class="sxs-lookup"><span data-stu-id="8ba9a-103">Using the Volume Shadow Copy Service</span></span>

<span data-ttu-id="8ba9a-104">Bei VSS-Sicherungs-und-Wiederherstellungs Vorgängen wird jeweils ein Protokoll für die Interaktion der Systeme verwendet, die Massenspeicher (Writer) verwenden, und diejenigen, die Sie sichern (Requester).</span><span class="sxs-lookup"><span data-stu-id="8ba9a-104">VSS backup and restore operations each use a protocol for the interaction of the systems that use mass storage (writers) and those that back it up (requesters).</span></span>

<span data-ttu-id="8ba9a-105">Sowohl Sicherungs-als auch Wiederherstellungs Vorgänge werden hauptsächlich von der anfordernden Person gesteuert, die das Verhalten von Writer und Anbietern steuert, indem systemweite com-Ereignisse für den Writer erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="8ba9a-105">Both backup and restore operations are primarily driven by the requester, which controls writer and provider behavior by generating systemwide COM events for the writer to process.</span></span> <span data-ttu-id="8ba9a-106">Da Ereignis generierende Methoden asynchron sind, haben Writer eine eingeschränkte Kontrolle über den Zustand des Anforderers über die für VSS verfügbaren asynchronen Handler (siehe [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span><span class="sxs-lookup"><span data-stu-id="8ba9a-106">Because event-generating methods are asynchronous, writers do have limited control into the requester's state through the asynchronous handlers available to VSS (see [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span></span>

<span data-ttu-id="8ba9a-107">Diese Interaktion erfordert grundlegende Datenstrukturen, die Dateien und Gruppen von Dateien ([*Komponenten*](vssgloss-c.md)) beschreiben, sowie ein Metadatenmodell, um die Speicherung von Sicherungs Informationen und die Kommunikation zwischen Writer und Anforderer zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="8ba9a-107">This interaction requires basic data structures describing files and groups of files ([*components*](vssgloss-c.md)), as well as a metadata model to allow the storage of backup information and to permit writer/requester communication.</span></span>

-   [<span data-ttu-id="8ba9a-108">VSS-Anwendungskompatibilität</span><span class="sxs-lookup"><span data-stu-id="8ba9a-108">VSS Application Compatibility</span></span>](usage-conventions.md)
-   [<span data-ttu-id="8ba9a-109">Konfigurieren von VSS</span><span class="sxs-lookup"><span data-stu-id="8ba9a-109">Configuring VSS</span></span>](configuring-vss.md)
-   [<span data-ttu-id="8ba9a-110">VSS-Metadaten</span><span class="sxs-lookup"><span data-stu-id="8ba9a-110">VSS Metadata</span></span>](vss-metadata.md)
-   [<span data-ttu-id="8ba9a-111">Arbeiten mit selekabilität und logischen Pfaden</span><span class="sxs-lookup"><span data-stu-id="8ba9a-111">Working with Selectability and Logical Paths</span></span>](working-with-selectability-and-logical-paths.md)
-   [<span data-ttu-id="8ba9a-112">Übersicht über die Verarbeitung einer Sicherung unter VSS</span><span class="sxs-lookup"><span data-stu-id="8ba9a-112">Overview of Processing a Backup Under VSS</span></span>](overview-of-processing-a-backup-under-vss.md)
-   [<span data-ttu-id="8ba9a-113">Übersicht über die Verarbeitung einer Wiederherstellung unter VSS</span><span class="sxs-lookup"><span data-stu-id="8ba9a-113">Overview of Processing a Restore Under VSS</span></span>](overview-of-processing-a-restore-under-vss.md)

 

 



