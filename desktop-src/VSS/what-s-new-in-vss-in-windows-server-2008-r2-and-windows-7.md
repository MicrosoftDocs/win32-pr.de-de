---
description: Mit Windows Server 2008 R2 und Windows 7 werden die folgenden Änderungen am Volumeschattenkopie-Dienst eingeführt.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Neuerungen: VSS in Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350442"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a><span data-ttu-id="a6491-103">Neuerungen: VSS in Windows Server 2008 R2 & Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6491-103">What's New: VSS in Windows Server 2008 R2 & Windows 7</span></span>

<span data-ttu-id="a6491-104">Mit Windows Server 2008 R2 und Windows 7 werden die folgenden Änderungen am Volumeschattenkopie-Dienst eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a6491-104">Windows Server 2008 R2 and Windows 7 introduce the following changes to the Volume Shadow Copy Service.</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="a6491-105">Neue VSS-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a6491-105">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="a6491-106">**IVssBackupComponentsEx3**</span><span class="sxs-lookup"><span data-stu-id="a6491-106">**IVssBackupComponentsEx3**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[<span data-ttu-id="a6491-107">**IVssComponentEx2**</span><span class="sxs-lookup"><span data-stu-id="a6491-107">**IVssComponentEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[<span data-ttu-id="a6491-108">**Ivsskreateexpressschreitermetadata**</span><span class="sxs-lookup"><span data-stu-id="a6491-108">**IVssCreateExpressWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[<span data-ttu-id="a6491-109">**Ivssexpresswriter**</span><span class="sxs-lookup"><span data-stu-id="a6491-109">**IVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a><span data-ttu-id="a6491-110">Neue VSS-Klassen</span><span class="sxs-lookup"><span data-stu-id="a6491-110">New VSS Classes</span></span>

<dl>

[<span data-ttu-id="a6491-111">**CVssWriterEx2**</span><span class="sxs-lookup"><span data-stu-id="a6491-111">**CVssWriterEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="a6491-112">Neue VSS-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="a6491-112">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="a6491-113">**VSS- \_ Wiederherstellungs \_ Optionen**</span><span class="sxs-lookup"><span data-stu-id="a6491-113">**VSS\_RECOVERY\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a><span data-ttu-id="a6491-114">Neue VSS-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a6491-114">New VSS Functions</span></span>

<dl>

[<span data-ttu-id="a6491-115">**"Kreatevssexpresswriter"**</span><span class="sxs-lookup"><span data-stu-id="a6491-115">**CreateVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="a6491-116">Vorhandene Änderungen der VSS-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a6491-116">Existing VSS Interface Modifications</span></span>

<dl>

<span data-ttu-id="a6491-117">[**Ivsshardwaresnapshotproviderex**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a6491-117">[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex) interface</span></span><dl> <span data-ttu-id="a6491-118">Hinzugefügte Methode: [ **resyncluns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span><span class="sxs-lookup"><span data-stu-id="a6491-118">Added method: [**ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span></span>  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="a6491-119">VSS-Ereignis Ablauf Verfolgung und Protokollierung</span><span class="sxs-lookup"><span data-stu-id="a6491-119">VSS Event Tracing and Logging</span></span>

<span data-ttu-id="a6491-120">Ab Windows Server 2008 R2 und Windows 7 können Sie das vsstrace-Tool, das Logman-Tool oder das tracelog-Tool verwenden, um Ablauf Verfolgungs Informationen für die VSS-Infrastruktur zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="a6491-120">Beginning with Windows Server 2008 R2 and Windows 7, you can use the VssTrace tool, the Logman tool, or the Tracelog tool to collect tracing information for the VSS infrastructure.</span></span> <span data-ttu-id="a6491-121">Weitere Informationen finden Sie unter [Verwenden von Ablauf Verfolgungs Tools mit VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="a6491-121">For more information, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="lun-resynchronization"></a><span data-ttu-id="a6491-122">LUN-Neusynchronisierung</span><span class="sxs-lookup"><span data-stu-id="a6491-122">LUN Resynchronization</span></span>

<span data-ttu-id="a6491-123">In Windows Server 2008 R2 und Windows 7 können VSS-Anforderer ein Hardwareschattenkopie-Anbieter-Feature namens LUN-Neusynchronisierung (oder LUN-Neusynchronisierung) verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6491-123">In Windows Server 2008 R2 and Windows 7, VSS requesters can use a hardware shadow copy provider feature called LUN resynchronization (or "LUN resync").</span></span> <span data-ttu-id="a6491-124">Dies ist ein schnelles Wiederherstellungs Schema, das es einem Anwendungs Administrator ermöglicht, Daten aus einer Schatten Kopie in die ursprüngliche logische Gerätenummer (Logical Unit Number, LUN) oder in eine neue LUN wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="a6491-124">This is a fast-recovery scheme that allows an application administrator to restore data from a shadow copy to the original logical unit number (LUN) or to a new LUN.</span></span> <span data-ttu-id="a6491-125">Bei der Schattenkopie kann es sich um einen vollständigen Klon oder eine differenzielle Schattenkopie handeln.</span><span class="sxs-lookup"><span data-stu-id="a6491-125">The shadow copy can be a full clone or a differential shadow copy.</span></span> <span data-ttu-id="a6491-126">In beiden Fällen hat die Ziel-LUN am Ende der erneuten Synchronisierung denselben Inhalt wie die Schattenkopie-LUN.</span><span class="sxs-lookup"><span data-stu-id="a6491-126">In either case, at the end of the resync operation, the destination LUN will have the same contents as the shadow copy LUN.</span></span> <span data-ttu-id="a6491-127">Während der erneuten Synchronisierung erstellt das Array eine Kopie auf Blockebene aus der Schattenkopie in die Ziel-LUN.</span><span class="sxs-lookup"><span data-stu-id="a6491-127">During the resync operation, the array performs a block-level copy from the shadow copy to the destination LUN.</span></span> <span data-ttu-id="a6491-128">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="a6491-128">For more information, see the following:</span></span>

-   [<span data-ttu-id="a6491-129">LUN Resync: ein schnelles Wiederherstellungs Szenario auf Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a6491-129">LUN Resync - A fast recovery scenario in Server 2008 R2</span></span>](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   <span data-ttu-id="a6491-130">"Wie Schatten Kopien verwendet werden" in [Volumeschattenkopie-Dienst](/windows-server/storage/file-server/volume-shadow-copy-service)</span><span class="sxs-lookup"><span data-stu-id="a6491-130">"How Shadow Copies Are Used" in [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service)</span></span>
-   [<span data-ttu-id="a6491-131">Allgemeine LUN-Neusynchronisierungs Probleme</span><span class="sxs-lookup"><span data-stu-id="a6491-131">Common LUN Resync gotchas</span></span>](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a><span data-ttu-id="a6491-132">Express Writer</span><span class="sxs-lookup"><span data-stu-id="a6491-132">Express Writers</span></span>

<span data-ttu-id="a6491-133">In Windows Server 2008 R2 und Windows 7 ermöglicht die VSS Express-Schnittstelle einer Anwendung, den Speicherort Ihrer Datendateien zu registrieren, ohne eine VSS Writer zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="a6491-133">In Windows Server 2008 R2 and Windows 7, the VSS express interface allows an application to register the location of its data files without implementing a VSS writer.</span></span> <span data-ttu-id="a6491-134">Weitere Informationen finden Sie unter [Volumeschattenkopie-Dienst (VSS) Express Writer](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span><span class="sxs-lookup"><span data-stu-id="a6491-134">For more information, see [Volume Shadow Copy Service (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span></span>

## <a name="new-vss-writers"></a><span data-ttu-id="a6491-135">Neue VSS-Writer</span><span class="sxs-lookup"><span data-stu-id="a6491-135">New VSS Writers</span></span>

<span data-ttu-id="a6491-136">Mit Windows Server 2008 R2 und Windows 7 werden die folgenden VSS-Writer eingeführt:</span><span class="sxs-lookup"><span data-stu-id="a6491-136">Windows Server 2008 R2 and Windows 7 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="a6491-137">Leistungsindikatoren Writer</span><span class="sxs-lookup"><span data-stu-id="a6491-137">Performance Counters Writer</span></span>
-   <span data-ttu-id="a6491-138">Taskplaner Writer</span><span class="sxs-lookup"><span data-stu-id="a6491-138">Task Scheduler Writer</span></span>
-   <span data-ttu-id="a6491-139">VSS-Metadatenspeicher-Writer</span><span class="sxs-lookup"><span data-stu-id="a6491-139">VSS Metadata Store Writer</span></span>

<span data-ttu-id="a6491-140">Diese neuen Writer sind in den [in-Box-VSS-Writern](in-box-vss-writers.md)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="a6491-140">These new writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
