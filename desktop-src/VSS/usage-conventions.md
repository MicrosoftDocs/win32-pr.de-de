---
description: Wenn Sie Ihre eigene VSS-Anwendung entwickeln, sollten Sie die folgenden Richtlinien und Einschränkungen beachten.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: VSS-Anwendungskompatibilität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343579"
---
# <a name="vss-application-compatibility"></a><span data-ttu-id="39a78-103">VSS-Anwendungskompatibilität</span><span class="sxs-lookup"><span data-stu-id="39a78-103">VSS Application Compatibility</span></span>

<span data-ttu-id="39a78-104">Wenn Sie Ihre eigene VSS-Anwendung entwickeln, sollten Sie die folgenden Richtlinien und Einschränkungen beachten.</span><span class="sxs-lookup"><span data-stu-id="39a78-104">When developing your own VSS application, you should observe the following guidelines and restrictions.</span></span> <span data-ttu-id="39a78-105">Möglicherweise ist es hilfreich, auf den Beispielcode für VSS-Anforderer, Anbieter und Writer zu verweisen, die im Microsoft Windows Software Development Kit (SDK) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="39a78-105">You may find it helpful to refer to the sample code for VSS requesters, providers, and writers that is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="39a78-106">Der Windows SDK kann verwendet werden, um VSS-Anwendungen nur für Windows Vista-und spätere Windows-Betriebssystemversionen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="39a78-106">The Windows SDK can be used to develop VSS applications only for Windows Vista and later Windows operating system versions.</span></span> <span data-ttu-id="39a78-107">Sie kann nicht verwendet werden, um VSS-Anforderer, Anbieter oder Writer für Windows Server 2003 R2, Windows Server 2003 oder Windows XP zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="39a78-107">It cannot be used to develop VSS requesters, providers, or writers for Windows Server 2003 R2, Windows Server 2003, or Windows XP.</span></span>

 

<span data-ttu-id="39a78-108">**Windows Server 2003 R2, Windows Server 2003 und Windows XP:** VSS ist im SDK für Volumeschattenkopie-Dienst 7,2 verfügbar, das Sie unter herunterladen können [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) .</span><span class="sxs-lookup"><span data-stu-id="39a78-108">**Windows Server 2003 R2, Windows Server 2003 and Windows XP:** VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="39a78-109">Beachten Sie, dass die 64-Bit-Vssapi. lib-Dateien in den Verzeichnissen unter dem \\ Verzeichnis Win2003 obj für die 64-Bit-Versionen von Windows Server 2003 R2, Windows Server 2003 und Windows XP verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="39a78-109">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 R2, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="39a78-110">Dieses SDK stellt außerdem Beispielcode für VSS-Anforderer, Anbieter und Writer bereit.</span><span class="sxs-lookup"><span data-stu-id="39a78-110">This SDK also provides sample code for VSS requesters, providers, and writers.</span></span>

## <a name="compiling-vss-applications"></a><span data-ttu-id="39a78-111">Kompilieren von VSS-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="39a78-111">Compiling VSS Applications</span></span>

<span data-ttu-id="39a78-112">Beim Entwickeln eines Anforderers, z. b. einer Sicherungs Anwendung:</span><span class="sxs-lookup"><span data-stu-id="39a78-112">When developing a requester, such as a backup application:</span></span>

-   <span data-ttu-id="39a78-113">Fügen Sie die folgenden Header ein:</span><span class="sxs-lookup"><span data-stu-id="39a78-113">Include the following headers:</span></span> <dl> <span data-ttu-id="39a78-114">VSS. h</span><span class="sxs-lookup"><span data-stu-id="39a78-114">Vss.h</span></span>  
    <span data-ttu-id="39a78-115">Vswriter. h</span><span class="sxs-lookup"><span data-stu-id="39a78-115">VsWriter.h</span></span>  
    <span data-ttu-id="39a78-116">Vsbackup. h</span><span class="sxs-lookup"><span data-stu-id="39a78-116">VsBackup.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="39a78-117">Vssapi. lib</span><span class="sxs-lookup"><span data-stu-id="39a78-117">VssApi.Lib</span></span>  
    </dl>

<span data-ttu-id="39a78-118">Wenn Sie einen Writer entwickeln:</span><span class="sxs-lookup"><span data-stu-id="39a78-118">When developing a writer:</span></span>

-   <span data-ttu-id="39a78-119">Fügen Sie die folgenden Header ein:</span><span class="sxs-lookup"><span data-stu-id="39a78-119">Include the following headers:</span></span> <dl> <span data-ttu-id="39a78-120">VSS. h</span><span class="sxs-lookup"><span data-stu-id="39a78-120">Vss.h</span></span>  
    <span data-ttu-id="39a78-121">Vswriter. h</span><span class="sxs-lookup"><span data-stu-id="39a78-121">VsWriter.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="39a78-122">Vssapi. lib</span><span class="sxs-lookup"><span data-stu-id="39a78-122">VssApi.lib</span></span>  
    </dl>

## <a name="supported-configurations-and-restrictions"></a><span data-ttu-id="39a78-123">Unterstützte Konfigurationen und Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="39a78-123">Supported Configurations and Restrictions</span></span>

<span data-ttu-id="39a78-124">In der folgenden Liste werden die unterstützten Konfigurationen und Einschränkungen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="39a78-124">The following list describes supported configurations and restrictions:</span></span>

-   <span data-ttu-id="39a78-125">VSS wird in Versionen des Windows-Betriebssystems ab Windows XP bereitgestellt und unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39a78-125">VSS is provided and supported on versions of the Windows operating system beginning with Windows XP.</span></span>
-   <span data-ttu-id="39a78-126">In der folgenden Tabelle werden Kompatibilitätsinformationen in Windows-Versionen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="39a78-126">The following table summarizes compatibility information across Windows versions.</span></span> <span data-ttu-id="39a78-127">Beachten Sie Folgendes: Wenn eine VSS-Anwendung "kompiliert für" eine angegebene Windows-Version ist, bedeutet dies, dass die Anwendung mit den Header Dateien und Bibliotheken kompiliert wurde, die für diese Version spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="39a78-127">Note that if a VSS application is "compiled for" a specified Windows version, this means that the application was compiled using the header files and libraries that are specific to that version.</span></span>

    > [!Note]  
    > <span data-ttu-id="39a78-128">Hardware Anbieter können nur unter Windows Server-Betriebssystemversionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="39a78-128">Hardware providers will run only on Windows server operating system versions.</span></span> <span data-ttu-id="39a78-129">Sie können nicht unter Versionen von Windows-Client Betriebssystemen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="39a78-129">They will not run on Windows client operating system versions.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="39a78-130">In den folgenden Tabellen sollte Windows Server 2008 mit Service Pack 2 (SP2) als identisch mit Windows Server 2008 betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="39a78-130">In the following tables, Windows Server 2008 with Service Pack 2 (SP2) should be considered the same as Windows Server 2008.</span></span> <span data-ttu-id="39a78-131">Weitere Informationen zu Windows Server 2008 mit SP2 finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=178730> .</span><span class="sxs-lookup"><span data-stu-id="39a78-131">For more information about Windows Server 2008 with SP2, see <https://go.microsoft.com/fwlink/p/?linkid=178730>.</span></span> <span data-ttu-id="39a78-132">Windows Server 2003 R2 sollte als identisch mit Windows Server 2003 betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="39a78-132">Windows Server 2003 R2 should be considered the same as Windows Server 2003.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="39a78-133">Wenn eine VSS-Anwendung für Windows Server 2003 oder höher kompiliert wird, wird Sie auch unter neueren Versionen von Windows ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39a78-133">If a VSS application is compiled for Windows Server 2003 or later, it will also run on later versions of Windows.</span></span>

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="39a78-134">VSS-Anforderer, Writer und Anbieter, die für kompiliert wurden</span><span class="sxs-lookup"><span data-stu-id="39a78-134">VSS requesters, writers, and providers compiled for</span></span></th>
    <th><span data-ttu-id="39a78-135">Wird ausgeführt auf</span><span class="sxs-lookup"><span data-stu-id="39a78-135">Will run on</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="39a78-136">Windows Server 2008 R2 (64 Bit), Windows 7 (64-Bit), Windows Server 2008 (64-Bit) und Windows Vista (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="39a78-136">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    <td><span data-ttu-id="39a78-137">Windows Server 2008 R2 (64 Bit), Windows 7 (64-Bit), Windows Server 2008 (64-Bit) und Windows Vista (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="39a78-137">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="39a78-138">Windows Server 2008 R2 (32 Bit), Windows 7 (32-Bit), Windows Server 2008 (32-Bit) und Windows Vista (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="39a78-138">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    <td><span data-ttu-id="39a78-139">Windows Server 2008 R2 (32 Bit), Windows 7 (32-Bit), Windows Server 2008 (32-Bit) und Windows Vista (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="39a78-139">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="39a78-140">Windows Server 2003 (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="39a78-140">Windows Server 2003 (64-bit)</span></span></td>
    <td><span data-ttu-id="39a78-141">Windows Server 2008 R2 (64-Bit), Windows 7 (64-Bit), Windows Server 2008 (64-Bit), Windows Vista (64 Bit) und Windows Server 2003 (64-Bit)</span><span class="sxs-lookup"><span data-stu-id="39a78-141">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit), Windows Vista (64-bit), and Windows Server 2003 (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="39a78-142">Windows Server 2003 (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="39a78-142">Windows Server 2003 (32-bit)</span></span></td>
    <td><span data-ttu-id="39a78-143">Windows Server 2008 R2 (32-Bit), Windows 7 (32-Bit), Windows Server 2008 (32-Bit), Windows Vista (32 Bit) und Windows Server 2003 (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="39a78-143">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit), Windows Vista (32-bit), and Windows Server 2003 (32-bit)</span></span> <blockquote>
    [!Note]<br />
<span data-ttu-id="39a78-144">Anfordernde Personen werden auch unter Windows Server 2003 (64-Bit) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39a78-144">Requesters will also run on Windows Server 2003 (64-bit).</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="39a78-145">Windows XP 64-Bit-Edition</span><span class="sxs-lookup"><span data-stu-id="39a78-145">Windows XP 64-Bit Edition</span></span></td>
    <td><span data-ttu-id="39a78-146">Windows Server 2003 (64 Bit) und Windows XP 64-Bit Edition</span><span class="sxs-lookup"><span data-stu-id="39a78-146">Windows Server 2003 (64-bit) and Windows XP 64-Bit Edition</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="39a78-147">Windows XP (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="39a78-147">Windows XP (32-bit)</span></span></td>
    <td><span data-ttu-id="39a78-148">Windows XP (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="39a78-148">Windows XP (32-bit)</span></span></td>
    </tr>
    </tbody>
    </table>

    

     

    

    | <span data-ttu-id="39a78-149">So kompilieren Sie eine VSS-Anforderer, einen Writer oder einen Anbieter für</span><span class="sxs-lookup"><span data-stu-id="39a78-149">To compile a VSS requester, writer, or provider for</span></span>        | <span data-ttu-id="39a78-150">Zweck</span><span class="sxs-lookup"><span data-stu-id="39a78-150">Use</span></span>                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="39a78-151">Windows Server 2008 R2 oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="39a78-151">Windows Server 2008 R2 or Windows 7</span></span>                        | <span data-ttu-id="39a78-152">Windows SDK für Windows 7 (verfügbar im [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).)</span><span class="sxs-lookup"><span data-stu-id="39a78-152">Windows SDK for Windows 7 (Available from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).)</span></span>                |
    | <span data-ttu-id="39a78-153">Windows Server 2008 oder Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39a78-153">Windows Server 2008 or Windows Vista</span></span>                       | <span data-ttu-id="39a78-154">Windows SDK für Windows Server 2008 (verfügbar über das [Windows SDK Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx).)</span><span class="sxs-lookup"><span data-stu-id="39a78-154">Windows SDK for Windows Server 2008 (Available from the [Windows SDK Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx).)</span></span> |
    | <span data-ttu-id="39a78-155">Windows Server 2003 R2, Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="39a78-155">Windows Server 2003 R2, Windows Server 2003, or Windows XP</span></span> | [<span data-ttu-id="39a78-156">Volumeschattenkopie-Dienst 7,2-SDK</span><span class="sxs-lookup"><span data-stu-id="39a78-156">Volume Shadow Copy Service 7.2 SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   <span data-ttu-id="39a78-157">Alle 32-Bit-VSS-Anwendungen (Requester, Anbieter und Writer) müssen als native 32-Bit-oder 64-Bit-Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="39a78-157">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="39a78-158">Die Ausführung unter WOW64 wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39a78-158">Running them under WOW64 is not supported.</span></span>

    <span data-ttu-id="39a78-159">**Windows Server 2003 und Windows XP:** Das Ausführen von 32-Bit-VSS-Anforderern unter WOW64 wird unterstützt, jedoch nicht für Sicherungen des Systemstatus.</span><span class="sxs-lookup"><span data-stu-id="39a78-159">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="39a78-160">Das Ausführen von 32-Bit-VSS-Anbietern und-Writern unter WOW64 wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39a78-160">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="39a78-161">Unterstützung für die Ausführung von 32-Bit-Anforderern unter WOW64 wurde in Windows Vista und nachfolgenden Versionen entfernt.</span><span class="sxs-lookup"><span data-stu-id="39a78-161">Support for running 32- bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

-   <span data-ttu-id="39a78-162">Eine Schatten Kopie, die auf Windows Server 2003 R2 oder Windows Server 2003 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2008 R2 oder Windows Server 2008 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39a78-162">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="39a78-163">Eine Schatten Kopie, die auf Windows Server 2008 R2 oder Windows Server 2008 erstellt wurde, kann nicht auf einem Computer verwendet werden, auf dem Windows Server 2003 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39a78-163">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="39a78-164">Eine Schatten Kopie, die auf Windows Server 2008 erstellt wurde, kann jedoch auf einem Computer verwendet werden, auf dem Windows Server 2008 R2 ausgeführt wird, und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="39a78-164">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>
-   <span data-ttu-id="39a78-165">Um Schatten Kopien zu unterstützen, muss ein System, auf dem VSS ausgeführt wird, mindestens ein NTFS-Dateisystem aufweisen.</span><span class="sxs-lookup"><span data-stu-id="39a78-165">To support shadow copies, a system running VSS must have at least one NTFS file system.</span></span> <span data-ttu-id="39a78-166">Dieses Dateisystem hostet den Bereich "diff" der Schatten Kopie.</span><span class="sxs-lookup"><span data-stu-id="39a78-166">This file system will host the shadow copy's "diff area."</span></span> <span data-ttu-id="39a78-167">Weitere Informationen finden Sie unter [System Anbieter](providers.md).</span><span class="sxs-lookup"><span data-stu-id="39a78-167">For more information, see [System Provider](providers.md).</span></span>
-   <span data-ttu-id="39a78-168">Aufgrund des Vorhandenseins eines NTFS-Dateisystems und der entsprechenden Auswahl von Kontext (siehe [Kontext Konfigurationen für Schatten Kopien](shadow-copy-context-configurations.md)) können alle unterstützten lokalen Dateisysteme mit Schatten Kopien kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="39a78-168">Given the presence of one NTFS file system, and given the appropriate choice of context (see [Shadow Copy Context Configurations](shadow-copy-context-configurations.md)), any supported local file system can be shadow copied.</span></span>
-   <span data-ttu-id="39a78-169">Sie können Schatten Kopien nur für lokal eingebundene Dateisysteme erstellen.</span><span class="sxs-lookup"><span data-stu-id="39a78-169">You can make shadow copies only for locally mounted file systems.</span></span> <span data-ttu-id="39a78-170">Remote Freigaben und andere bereitgestellte Dateisysteme können von dem System, von dem Sie bereitgestellt werden, nicht durch Schatten Kopien kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="39a78-170">Remote shares and other cross-mounted file systems cannot be shadow copied by the system that mounts them.</span></span> <span data-ttu-id="39a78-171">Diese Dateisysteme können nur von den Systemen, die die Dateisysteme bedienen, als Schatten Kopien kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="39a78-171">These file systems can be shadow copied only by the systems that serve out the file systems.</span></span>
-   <span data-ttu-id="39a78-172">Writer und Anforderer sollten nur lokale Ressourcen angeben.</span><span class="sxs-lookup"><span data-stu-id="39a78-172">Writers and requesters should specify only local resources.</span></span> <span data-ttu-id="39a78-173">Lokale Ressourcen sind Sätze von Dateien, deren absoluter Pfad mit einem Laufwerk Buchstaben beginnt und der Laufwerk Buchstabe einem bereitgestellten Ordner auf einer Remote Freigabe nicht zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="39a78-173">Local resources are sets of files whose absolute path starts with a drive letter, and the drive letter cannot be associated with a mounted folder on a remote share.</span></span>
-   <span data-ttu-id="39a78-174">Die maximale Anzahl von Software Schatten Kopien beträgt 512.</span><span class="sxs-lookup"><span data-stu-id="39a78-174">The maximum number is of software shadow copies for each volume is 512.</span></span> <span data-ttu-id="39a78-175">Standardmäßig können Sie jedoch nur 64 Schattenkopien verwalten, die vom Feature „Schattenkopien von freigegebenen Ordnern“ verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39a78-175">However, by default you can only maintain 64 shadow copies that are used by the Shadow Copies of Shared Folders feature.</span></span> <span data-ttu-id="39a78-176">Verwenden Sie den Registrierungsschlüssel " [maxshadowkopien](../backup/registry-keys-for-backup-and-restore.md) ", um das Limit für die Funktion "Schatten Kopien von freigegebenen Ordnern" zu ändern.</span><span class="sxs-lookup"><span data-stu-id="39a78-176">To change the limit for the Shadow Copies of Shared Folders feature, use the [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) registry key.</span></span>
-   <span data-ttu-id="39a78-177">Die Sicherungs Komponenten Infrastruktur unterstützt nicht das Sichern von Cluster Ressourcen als Writer-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="39a78-177">The Backup Components infrastructure does not support backing up cluster resources as writer components.</span></span> <span data-ttu-id="39a78-178">Zum Sichern von Cluster Ressourcen sollten Anwendungen davon ausgehen, dass der Pfad für einen bestimmten Cluster Knoten lokal ist.</span><span class="sxs-lookup"><span data-stu-id="39a78-178">To back up cluster resources, applications should assume that the path is local to a specified particular cluster node.</span></span>
-   [!Note]  
    > <span data-ttu-id="39a78-179">Microsoft bietet keinen technischen Support für Entwickler oder IT-Experten für die Implementierung von Online-Systemstatus Wiederherstellungen unter Windows (alle Versionen).</span><span class="sxs-lookup"><span data-stu-id="39a78-179">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

     

    <span data-ttu-id="39a78-180">Wenn Sie den Systemstatus sichern und wiederherstellen, empfiehlt es sich, zusätzlich zu den Dateien, die von den systemstatuswritern aufgelistet werden, die System-und Startvolumes zu sichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="39a78-180">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span>

    > [!Note]  
    > <span data-ttu-id="39a78-181">Systemstatuswriter sind Writer, für die das [**VSS \_ Usage \_ Type**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) -Attribut entweder auf VSS- \_ UT \_ bootablesystemstate oder VSS \_ UT \_ Systemservice festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="39a78-181">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

     

 

 
