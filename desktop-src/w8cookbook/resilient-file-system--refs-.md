---
title: Robustes Dateisystem
description: Robustes Dateisystem
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "104039785"
---
# <a name="resilient-file-system"></a><span data-ttu-id="9b8b4-103">Robustes Dateisystem</span><span class="sxs-lookup"><span data-stu-id="9b8b4-103">Resilient file system</span></span>

## <a name="platform"></a><span data-ttu-id="9b8b4-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="9b8b4-104">Platform</span></span>

<span data-ttu-id="9b8b4-105">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b8b4-105">**Servers** – Windows Server 2012</span></span> 

## <a name="description"></a><span data-ttu-id="9b8b4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b8b4-106">Description</span></span>

<span data-ttu-id="9b8b4-107">Resilientes Dateisystem (Refs) ist ein neues lokales Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-107">Resilient File System (ReFS) is a new local file system.</span></span> <span data-ttu-id="9b8b4-108">Es maximiert die Datenverfügbarkeit, trotz der Fehler, die in der Vergangenheit zu Datenverlust oder Ausfallzeiten führen würden.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-108">It maximizes data availability, despite errors that would historically cause data loss or downtime.</span></span> <span data-ttu-id="9b8b4-109">Mit der Datenintegrität wird sichergestellt, dass geschäftskritische Daten vor Fehlern geschützt werden und bei Bedarf verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-109">Data integrity ensures that business critical data is protected from errors and available when needed.</span></span> <span data-ttu-id="9b8b4-110">Die Architektur ist so konzipiert, dass Sie Skalierbarkeit und Leistung in einem Zeitraum von ständig wachsenden DataSet-Größen und dynamischen Workloads bietet.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-110">Its architecture is designed to provide scalability and performance in an era of constantly growing data set sizes and dynamic workloads.</span></span>

<span data-ttu-id="9b8b4-111">Die wichtigsten Features von refs sind:</span><span class="sxs-lookup"><span data-stu-id="9b8b4-111">The key features of ReFS are:</span></span>

-   <span data-ttu-id="9b8b4-112">**Integrität**: Refs speichert Daten so, dass Sie vor vielen häufigen Fehlern geschützt werden, die zu Datenverlusten führen können.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-112">**Integrity**: ReFS stores data so that it is protected from many of the common errors that can cause data loss.</span></span> <span data-ttu-id="9b8b4-113">Dateisystem Metadaten sind immer geschützt.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-113">File system metadata is always protected.</span></span> <span data-ttu-id="9b8b4-114">Optional können Benutzerdaten auf Volumen-, Verzeichnis-oder Datei Basis geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-114">Optionally, user data can be protected on a per-volume, per-directory, or per-file basis.</span></span> <span data-ttu-id="9b8b4-115">Wenn eine Beschädigung auftritt, können Refs die Beschädigung erkennen und bei der Konfiguration mit Speicherplätzen automatisch korrigieren.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-115">If corruption occurs, ReFS can detect and, when configured with Storage Spaces, automatically correct the corruption.</span></span> <span data-ttu-id="9b8b4-116">Im Falle eines Systemfehlers ist Refs so konzipiert, dass dieser Fehler schnell wieder hergestellt werden kann, ohne dass Benutzerdaten verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-116">In the event of a system error, ReFS is designed to recover from that error rapidly, with no loss of user data.</span></span>
-   <span data-ttu-id="9b8b4-117">**Verfügbarkeit**: Refs wurde entwickelt, um die Verfügbarkeit von Daten zu priorisieren.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-117">**Availability**: ReFS is designed to prioritize the availability of data.</span></span> <span data-ttu-id="9b8b4-118">Wenn bei Refs eine Beschädigung auftritt und Sie nicht automatisch repariert werden kann, wird der Prozess der Online Rettung in den Bereich der Beschädigung lokalisiert, sodass keine Ausfallzeit des Volumes erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-118">With ReFS, if corruption occurs, and it cannot be repaired automatically, the online salvage process is localized to the area of corruption, requiring no volume down-time.</span></span> <span data-ttu-id="9b8b4-119">Kurz gesagt, wenn eine Beschädigung auftritt, bleiben Refs online.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-119">In short, if corruption occurs, ReFS will stay online.</span></span>
-   <span data-ttu-id="9b8b4-120">**Skalierbarkeit**: Refs ist für die DataSet-Größen von heute und die DataSet-Größen von Morgen vorgesehen. Es ist für eine hohe Skalierbarkeit optimiert.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-120">**Scalability**: ReFS is designed for the data set sizes of today and the data set sizes of tomorrow; it’s optimized for high scalability.</span></span>
-   <span data-ttu-id="9b8b4-121">**APP-Kompatibilität**: um AppCompat zu maximieren, unterstützt Refs eine Teilmenge der NTFS-Features und Win32-APIs, die weitgehend übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-121">**App Compatibility**: To maximize AppCompat, ReFS supports a subset of NTFS features plus Win32 APIs that are widely adopted.</span></span>
-   <span data-ttu-id="9b8b4-122">**Proaktive Fehler Identifikation**: die Integritäts Funktionen von refs werden von einem Daten Integritäts Scanner ("Scrubber") genutzt, der regelmäßig das Volume scannt, versucht, eine latente Beschädigung zu erkennen, und löst dann proaktiv eine Reparatur dieser beschädigten Daten aus.</span><span class="sxs-lookup"><span data-stu-id="9b8b4-122">**Proactive Error Identification**: The integrity capabilities of ReFS are leveraged by a data integrity scanner (a “scrubber”) that periodically scans the volume, attempts to identify latent corruption, and then proactively triggers a repair of that corrupt data.</span></span>

## <a name="resources"></a><span data-ttu-id="9b8b4-123">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9b8b4-123">Resources</span></span>

-   [<span data-ttu-id="9b8b4-124">Blog Beitrag zum Entwickeln von Windows 8 – entwickeln der nächsten Generation des Dateisystems für Windows: Refs</span><span class="sxs-lookup"><span data-stu-id="9b8b4-124">Building Windows 8 Blog Post – Building the next generation file system for Windows: ReFS</span></span>](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [<span data-ttu-id="9b8b4-125">Anwendungs Kompatibilität und Refs</span><span class="sxs-lookup"><span data-stu-id="9b8b4-125">Application Compatibility and ReFS</span></span>](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 