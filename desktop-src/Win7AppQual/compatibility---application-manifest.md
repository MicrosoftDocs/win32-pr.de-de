---
description: .
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Anwendungsmanifest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4fd1ae8a9f66dafbe65a3db09dd014dbef31e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366213"
---
# <a name="application-manifest"></a><span data-ttu-id="e57e0-103">Anwendungsmanifest</span><span class="sxs-lookup"><span data-stu-id="e57e0-103">Application Manifest</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e57e0-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="e57e0-104">Affected Platforms</span></span>

<span data-ttu-id="e57e0-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="e57e0-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="e57e0-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e57e0-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="e57e0-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="e57e0-107">Feature Impact</span></span>

 <span data-ttu-id="e57e0-108">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="e57e0-108">**Severity** - Low</span></span>  
<span data-ttu-id="e57e0-109">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="e57e0-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="e57e0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e57e0-110">Description</span></span>

<span data-ttu-id="e57e0-111">Mit Windows 7 wird ein neuer Abschnitt im Anwendungs Manifest mit dem Namen "Kompatibilität" eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e57e0-111">Windows 7 introduces a new section in the application manifest called "Compatibility."</span></span> <span data-ttu-id="e57e0-112">In diesem Abschnitt können Windows die Versionen von Windows ermitteln, für die eine Anwendung konzipiert wurde, und Windows das Verhalten bereitstellen, das die Anwendung basierend auf der Windows-Version erwartet, auf die die Anwendung ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="e57e0-112">This section helps Windows determine the versions of Windows that an application was designed to target, and enables Windows to provide the behavior that the application expects based on the version of Windows that the application targeted.</span></span>

<span data-ttu-id="e57e0-113">Im Kompatibilitäts Abschnitt können Windows neuen, von Entwicklern erstellten Software neuen Verhalten bereitstellen und gleichzeitig die Kompatibilität vorhandener Software beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e57e0-113">The Compatibility section allows Windows to provide new behavior to new developer-created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="e57e0-114">In diesem Abschnitt wird Windows auch bei zukünftigen Versionen von Windows mehr Kompatibilität bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e57e0-114">This section also helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="e57e0-115">Beispielsweise wird eine Anwendung, die die Unterstützung nur für Windows 7 im Kompatibilitäts Abschnitt deklariert, weiterhin Windows 7-Verhalten in zukünftigen Versionen von Windows empfangen.</span><span class="sxs-lookup"><span data-stu-id="e57e0-115">For example, an application declaring support only for Windows 7 in the Compatibility section will continue to receive Windows 7 behavior in future version of Windows.</span></span>

## <a name="manifestation-of-change"></a><span data-ttu-id="e57e0-116">Darstellung der Änderung</span><span class="sxs-lookup"><span data-stu-id="e57e0-116">Manifestation of Change</span></span>

<span data-ttu-id="e57e0-117">Anwendungen ohne Kompatibilitäts Abschnitt in ihrem Manifest erhalten standardmäßig Windows Vista-Verhalten unter Windows 7 und zukünftigen Windows-Versionen.</span><span class="sxs-lookup"><span data-stu-id="e57e0-117">Applications without a Compatibility section in their manifest will receive Windows Vista behavior by default on Windows 7 and future Windows versions.</span></span> <span data-ttu-id="e57e0-118">Beachten Sie, dass Windows XP und Windows Vista diesen Manifest-Abschnitt ignorieren und keine Auswirkung auf diese haben.</span><span class="sxs-lookup"><span data-stu-id="e57e0-118">Note that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="e57e0-119">Die folgenden Windows-Komponenten bieten unterschiedliche Verhaltensweisen auf der Grundlage des Kompatibilitäts Abschnitts in Windows 7:</span><span class="sxs-lookup"><span data-stu-id="e57e0-119">The following Windows components provide divergent behavior based on the Compatibility section in Windows 7:</span></span>

<span data-ttu-id="e57e0-120">**RPC-Standard Thread Pool**</span><span class="sxs-lookup"><span data-stu-id="e57e0-120">**RPC Default Thread Pool**</span></span>

-   <span data-ttu-id="e57e0-121">**Windows 7:** Um die Skalierbarkeit zu verbessern und die Thread Anzahl zu reduzieren, wechselt der RPC zum NT-Thread Pool (Standard Pool).</span><span class="sxs-lookup"><span data-stu-id="e57e0-121">**Windows 7:** To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="e57e0-122">Für Windows Vista hat RPC einen privaten Thread Pool verwendet.</span><span class="sxs-lookup"><span data-stu-id="e57e0-122">For Windows Vista, RPC used a private thread pool.</span></span>
    -   <span data-ttu-id="e57e0-123">Für Binärdateien, die für Win7 kompiliert werden, wird der Standard Pool verwendet.</span><span class="sxs-lookup"><span data-stu-id="e57e0-123">For binaries compiled for Win7 the default pool is used</span></span>
    -   <span data-ttu-id="e57e0-124">Wenn \_ RpcMgmtEnableDedicatedThreadPool aufgerufen wird, bevor eine RPC-API aufgerufen wird, wird der private Thread Pool verwendet (Vista-Verhalten).</span><span class="sxs-lookup"><span data-stu-id="e57e0-124">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior)</span></span>
    -   <span data-ttu-id="e57e0-125">Wenn ich \_ RpcMgmtEnableDedicatedThreadPool nach einem RPC-Aufruf aufgerufen wird, wird der Standard Pool verwendet. i \_ RpcMgmtEnableDedicatedThreadPool gibt den Fehler 1764 zurück, und der angeforderte Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e57e0-125">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported</span></span>
-   <span data-ttu-id="e57e0-126">**Windows Vista (Standard):** Für Binärdateien, die für Windows Vista und niedriger kompiliert werden, wird der private Pool verwendet.</span><span class="sxs-lookup"><span data-stu-id="e57e0-126">**Windows Vista (default):** For binaries compiled for Windows Vista and below, the private pool is used.</span></span>

<span data-ttu-id="e57e0-127">**DirectDraw-Sperre**</span><span class="sxs-lookup"><span data-stu-id="e57e0-127">**DirectDraw Lock**</span></span>

-   <span data-ttu-id="e57e0-128">**Windows 7:** Für Windows 7 manifestierte Anwendungen können die Lock-API in ddraw nicht aufrufen, um den primären Desktop-Video Puffer zu sperren.</span><span class="sxs-lookup"><span data-stu-id="e57e0-128">**Windows 7:** Applications manifested for Windows 7 cannot call Lock API in DDRAW to lock the primary Desktop video buffer.</span></span> <span data-ttu-id="e57e0-129">Dies führt zu einem Fehler, und für das primäre Replikat wird ein **null** -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e57e0-129">Doing so will result in error, and **NULL** pointer for the primary will be returned.</span></span> <span data-ttu-id="e57e0-130">Dieses Verhalten wird auch dann erzwungen, wenn Desktopfenster-Manager Komposition nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e57e0-130">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="e57e0-131">Windows 7-kompatible Anwendungen dürfen den primären Video Puffer nicht zum renderingsperren sperren.</span><span class="sxs-lookup"><span data-stu-id="e57e0-131">Windows 7 compatible applications must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="e57e0-132">**Windows Vista (Standard):** Anwendungen können eine Sperre für den primären Video Puffer erhalten, da ältere Anwendungen von diesem Verhalten abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="e57e0-132">**Windows Vista (default):** Applications will be able to acquire a lock on the primary video buffer as legacy applications depend on this behavior.</span></span> <span data-ttu-id="e57e0-133">Wenn Sie die Anwendung ausführen, wird Desktopfenster-Manager deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e57e0-133">Running the application turns off Desktop Window Manager.</span></span>

<span data-ttu-id="e57e0-134">**DirectDraw-Bitblock Übertragung (BLT) zum primären Replikat ohne Clipping-Fenster**</span><span class="sxs-lookup"><span data-stu-id="e57e0-134">**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**</span></span>

-   <span data-ttu-id="e57e0-135">**Windows 7:** Anwendungen, die für Windows 7 angezeigt werden, werden daran gehindert, BLT auf dem primären Desktop-Video Puffer ohne clippingfenster auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e57e0-135">**Windows 7:** Applications manifested for Windows 7 are prevented from performing Blt's to the primary Desktop video buffer without a clipping window.</span></span> <span data-ttu-id="e57e0-136">Dies führt zu einem Fehler, und der BLT-Bereich wird nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="e57e0-136">Doing so will result in error and the Blt area will not be rendered.</span></span> <span data-ttu-id="e57e0-137">Windows erzwingt dieses Verhalten auch dann, wenn Sie Desktopfenster-Manager Komposition nicht aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e57e0-137">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="e57e0-138">Windows 7-kompatible Anwendungen müssen in ein clippingfenster geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e57e0-138">Windows 7 compatible applications must Blt to a clipping window.</span></span>
-   <span data-ttu-id="e57e0-139">**Windows Vista (Standard):** Anwendungen müssen in der Lage sein, BLT zum primären Replikat ohne Clipping-Fenster zu haben, da ältere Anwendungen von diesem Verhalten abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="e57e0-139">**Windows Vista (default):** Applications must be able to Blt to the primary without a clipping window as legacy applications depend on this behavior.</span></span> <span data-ttu-id="e57e0-140">Wenn Sie diese Anwendung ausführen, wird der Desktopfenster-Manager deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e57e0-140">Running this application turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="e57e0-141">**Ge-verlappedresult-API**</span><span class="sxs-lookup"><span data-stu-id="e57e0-141">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="e57e0-142">**Windows 7:** Löst eine Racebedingung auf, bei der eine Multithread-APP, die gezu verlappedresult verwendet, zurückgegeben werden kann, ohne das Ereignis in der überlappenden Struktur zurückzusetzen, wodurch der nächste Aufrufe dieser Funktion vorzeitig zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e57e0-142">**Windows 7:** Resolves a race condition where a multithreaded app using GetOverlappedResult can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="e57e0-143">**Windows Vista (Standard):** Stellt das Verhalten mit der Racebedingung bereit, von der Anwendungen möglicherweise abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="e57e0-143">**Windows Vista (default):** Provides the behavior with the race condition that applications may have a dependency on.</span></span> <span data-ttu-id="e57e0-144">Anwendungen, die dieses Race vor dem Windows 7-Verhalten vermeiden möchten, sollten auf das überlappende Ereignis warten und, wenn signalisiert, gefliverlappedresult mit bwait = = **false** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e57e0-144">Applications wishing to avoid this race prior to the Windows 7 behavior should wait on the overlapped event and when signaled, call GetOverlappedResult with bWait == **FALSE**.</span></span>

<span data-ttu-id="e57e0-145">**Programmkompatibilitäts-Assistent (PCA)**</span><span class="sxs-lookup"><span data-stu-id="e57e0-145">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="e57e0-146">**Windows 7:** Anwendungen mit Kompatibilitäts Abschnitt erhalten keine PCA-Entschärfung.</span><span class="sxs-lookup"><span data-stu-id="e57e0-146">**Windows 7:** Applications with Compatibility section will not get the PCA mitigation.</span></span>
-   <span data-ttu-id="e57e0-147">**Windows Vista (Standard):** Anwendungen, die unter bestimmten Umständen nicht ordnungsgemäß installiert werden oder während der Laufzeit abstürzen, erhalten die PCA-Entschärfung.</span><span class="sxs-lookup"><span data-stu-id="e57e0-147">**Windows Vista (default):** Applications that fail to install properly or crash during runtime under some specific circumstances will get the PCA mitigation.</span></span> <span data-ttu-id="e57e0-148">Weitere Informationen finden Sie im Abschnitt "Reference".</span><span class="sxs-lookup"><span data-stu-id="e57e0-148">For more details, see the reference section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="e57e0-149">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="e57e0-149">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="e57e0-150">Aktualisieren Sie das Anwendungs Manifest mit den neuesten Kompatibilitätsinformationen für die Betriebssystemunterstützung.</span><span class="sxs-lookup"><span data-stu-id="e57e0-150">Update the application manifest with the latest Compatibility information for operating system support.</span></span> <span data-ttu-id="e57e0-151">In diesem Abschnitt werden die Ergänzungen des Manifests beschrieben:</span><span class="sxs-lookup"><span data-stu-id="e57e0-151">The section describes the additions to the manifest:</span></span>

-   <span data-ttu-id="e57e0-152">**Namespace:** Compatibility. v1 (xmlns = "urn: Schemas-Microsoft-com: Compatibility. v1" >)</span><span class="sxs-lookup"><span data-stu-id="e57e0-152">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

-   <span data-ttu-id="e57e0-153">**Abschnitts Name:** Kompatibilität (neuer Abschnitt)</span><span class="sxs-lookup"><span data-stu-id="e57e0-153">**Section Name:** Compatibility (new section)</span></span>

-   <span data-ttu-id="e57e0-154">**SupportedOS:** GUID des unterstützten Betriebssystems: die GUIDs, die den unterstützten Betriebssystemen zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="e57e0-154">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

    -   <span data-ttu-id="e57e0-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} für Windows Vista: Dies ist der Standardwert für den switchbackkontext.</span><span class="sxs-lookup"><span data-stu-id="e57e0-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} for Windows Vista: This is the default value for the switchback context.</span></span>
    -   <span data-ttu-id="e57e0-156">{35138b9a-5d96-4sbd-8e2d-a2440225t93a} für Windows 7: Anwendungen, die diesen Wert im Anwendungs Manifest festlegen, erhalten das Windows 7-Verhalten.</span><span class="sxs-lookup"><span data-stu-id="e57e0-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} for Windows 7: Applications that set this value in the application manifest get the Windows 7 behavior.</span></span>

    > [!Note]  
    > <span data-ttu-id="e57e0-157">Microsoft generiert und veröffentlicht GUIDs für zukünftige Windows-Versionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="e57e0-157">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

     

<span data-ttu-id="e57e0-158">Im folgenden finden Sie ein Beispiel für ein aktualisiertes Manifest.</span><span class="sxs-lookup"><span data-stu-id="e57e0-158">The following is an example of an updated manifest.</span></span>

> [!Note]  
> <span data-ttu-id="e57e0-159">Bei den Attribut-und Tagnamen im Anwendungs Manifest wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="e57e0-159">The attribute and tag names in the application manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



<span data-ttu-id="e57e0-160">Der Wert für das Hinzufügen von GUIDs für beide Betriebssysteme im obigen Beispiel ist die Bereitstellung einer Unterstützung von Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="e57e0-160">The value of adding GUIDs for both operating systems in the above example is to provide down-level support.</span></span> <span data-ttu-id="e57e0-161">Anwendungen, die beide Plattformen unterstützen, benötigen für jede Plattform keine separaten Manifeste.</span><span class="sxs-lookup"><span data-stu-id="e57e0-161">Applications that support both platforms would not need separate manifests for each platform.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="e57e0-162">Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="e57e0-162">Compatibility, Performance, Reliability, and Usability Testing</span></span>

1.  <span data-ttu-id="e57e0-163">Testen Sie die Anwendung mit dem neuen Kompatibilitäts Abschnitt `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` , und stellen Sie sicher, dass die Anwendung mit dem aktuellen Windows 7-Verhalten ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e57e0-163">Test the application with the new compatibility section and `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` to ensure that the application works properly using the latest Windows 7 behavior</span></span>
2.  <span data-ttu-id="e57e0-164">Testen Sie die Anwendung mit dem neuen Kompatibilitäts Abschnitt und `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (bzw. ohne diesen Abschnitt vollständig), um sicherzustellen, dass die Anwendung mit dem Windows Vista-Verhalten unter Windows 7 ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e57e0-164">Test the application with the new compatibility section and `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (or without this section entirely) to ensure that the application works properly using the Windows Vista behaviors on Windows 7</span></span>

## <a name="known-issues"></a><span data-ttu-id="e57e0-165">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="e57e0-165">Known Issues</span></span>

<span data-ttu-id="e57e0-166">**Kontext** Konflikt Eine Anwendung wird in einem Windows Vista-Kontext statt in einem Windows 7-Kontext auf einem Computer ausgeführt, auf dem eine x64-Edition von Windows 7 oder Windows Server 2008 R2 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e57e0-166">**Context Mismatch** An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of either Windows 7 or Windows Server 2008 R2.</span></span>

<span data-ttu-id="e57e0-167">**Lösung** Updates sind verfügbar, um dies für alle unterstützten x64-basierten Versionen von Windows 7 und Windows Server 2008 R2 sowie für alle unterstützten Itanium-basierten Versionen von Windows Server 2008 R2 zu beheben.</span><span class="sxs-lookup"><span data-stu-id="e57e0-167">**Solution** Updates are available to correct this for all supported x64-based versions of Windows 7 and Windows Server 2008 R2, as well as for all supported Itanium-based versions of Windows Server 2008 R2.</span></span> <span data-ttu-id="e57e0-168">Wechseln Sie zur Microsoft-Support Seite für [KB 978637: eine Anwendung wird in einem Windows Vista-Kontext statt in einem Windows 7-Kontext auf einem Computer ausgeführt, auf dem eine x64-Edition von Windows 7 oder Windows Server 2008 R2 ausgeführt wird](https://support.microsoft.com/kb/978637) , um weitere Informationen zu erhalten und die richtige Version für Ihr System herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="e57e0-168">Go to the Microsoft Support page for [KB 978637: An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of Windows 7 or of Windows Server 2008 R2](https://support.microsoft.com/kb/978637) for additional details and to download the correct version for your system.</span></span>

<span data-ttu-id="e57e0-169">**Absturz Abbild Diagnose blockiert**</span><span class="sxs-lookup"><span data-stu-id="e57e0-169">**Crash dump diagnosis blocked**</span></span>

<span data-ttu-id="e57e0-170">**Lösung** Wechseln Sie zur Microsoft-Support Seite für [KB 976038: Ausnahmen, die von einer Anwendung ausgelöst werden, die in einer 64-Bit-Version von Windows ausgeführt wird, werden](https://support.microsoft.com/kb/976038) bei zusätzlichen Details ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e57e0-170">**Solution** Go to the Microsoft Support page for [KB 976038: Exceptions that are thrown from an application that runs in a 64-bit version of Windows are ignored](https://support.microsoft.com/kb/976038) for additional details.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="e57e0-171">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e57e0-171">Links to Other Resources</span></span>

-   [<span data-ttu-id="e57e0-172">**Queryactctxw-Funktion**</span><span class="sxs-lookup"><span data-stu-id="e57e0-172">**QueryActCtxW Function**</span></span>](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   <span data-ttu-id="e57e0-173">[UAC-Manifest](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e57e0-173">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="e57e0-174">Anwendungs Manifeste für Windows-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e57e0-174">Application manifests for Windows applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="e57e0-175">Desktopfenster-Manager (DWM)</span><span class="sxs-lookup"><span data-stu-id="e57e0-175">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="e57e0-176">Aktualisierung des Kontext Konflikts</span><span class="sxs-lookup"><span data-stu-id="e57e0-176">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)

 

 
