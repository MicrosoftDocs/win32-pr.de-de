---
title: App-Manifest (ausführbare Datei)
description: App-Manifest (ausführbare Datei)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039735"
---
# <a name="app-executable-manifest"></a><span data-ttu-id="c9ad3-103">App-Manifest (ausführbare Datei)</span><span class="sxs-lookup"><span data-stu-id="c9ad3-103">App (executable) manifest</span></span>

## <a name="platforms"></a><span data-ttu-id="c9ad3-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="c9ad3-104">Platforms</span></span>

<span data-ttu-id="c9ad3-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="c9ad3-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="c9ad3-106">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9ad3-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="c9ad3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9ad3-107">Description</span></span>

<span data-ttu-id="c9ad3-108">Der Kompatibilitäts Abschnitt des in Windows eingeführten App-Manifests (ausführbare Datei) unterstützt das Betriebssystem bei der Ermittlung der Windows-Versionen, für die eine APP entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-108">The compatibility section of the app (executable) manifest introduced in Windows helps the operating system determine the versions of Windows an app was designed to target.</span></span> <span data-ttu-id="c9ad3-109">Außerdem ermöglicht das App-Manifest Windows, das von der APP erwartete Verhalten basierend auf der Version von Windows, die die APP als Ziel hat, bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-109">Additionally, the app manifest enables Windows to provide the behavior that the app expects based on the version of Windows that the app targeted.</span></span>

<span data-ttu-id="c9ad3-110">Im Kompatibilitäts Abschnitt des Manifests können Windows neue Verhaltensweisen für neu erstellte Software bereitstellen und gleichzeitig die Kompatibilität vorhandener Software beibehalten.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-110">The compatibility section of the manifest allows Windows to provide new behavior to newly created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="c9ad3-111">In diesem Abschnitt wird Windows auch bei zukünftigen Versionen von Windows mehr Kompatibilität bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-111">This section helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="c9ad3-112">Beispielsweise wird eine APP, die Unterstützung nur für Windows 8 im Kompatibilitäts Abschnitt deklariert, weiterhin Windows 8-Verhalten in zukünftigen Versionen von Windows empfangen.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-112">For example, an app declaring support for only Windows 8 in the compatibility section will continue to receive Windows 8 behavior in future versions of Windows.</span></span>

## <a name="manifestation"></a><span data-ttu-id="c9ad3-113">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="c9ad3-113">Manifestation</span></span>

<span data-ttu-id="c9ad3-114">Apps ohne Kompatibilitäts Abschnitt in ihrem Manifest haben standardmäßig Windows Vista-Verhalten unter Windows 7 und Windows 8 und zukünftigen Windows-Versionen.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-114">Apps without a compatibility section in their manifest will have Windows Vista behavior by default on Windows 7 and Windows 8 and future Windows versions.</span></span> <span data-ttu-id="c9ad3-115">Beachten Sie, dass diese Manifestressourcen von Windows XP und Windows Vista ignoriert werden und keine Auswirkung darauf besteht.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-115">Be aware that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="c9ad3-116">Diese Windows-Komponenten bieten unterschiedliche Verhaltensweisen auf der Grundlage des Kompatibilitäts Abschnitts:</span><span class="sxs-lookup"><span data-stu-id="c9ad3-116">These Windows components provide divergent behavior based on the compatibility section:</span></span>

<span data-ttu-id="c9ad3-117">**Remote Prozedur Aufruf (RPC)-Standard Thread Pool**</span><span class="sxs-lookup"><span data-stu-id="c9ad3-117">**Remote procedure call (RPC) default thread pool**</span></span>

-   <span data-ttu-id="c9ad3-118">Windows 8 und Windows 7: um die Skalierbarkeit zu verbessern und die Thread Anzahl zu reduzieren, wechselt der RPC zum NT-Thread Pool (Standard Pool).</span><span class="sxs-lookup"><span data-stu-id="c9ad3-118">Windows 8 and Windows 7: To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="c9ad3-119">Für Windows Vista hat RPC einen privaten Thread Pool verwendet:</span><span class="sxs-lookup"><span data-stu-id="c9ad3-119">For Windows Vista, RPC used a private thread pool:</span></span>

    -   <span data-ttu-id="c9ad3-120">Für Binärdateien, die für Windows 7 und spätere Versionen von Windows kompiliert wurden, wird der Standard Pool verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-120">For binaries compiled for Windows 7 and later versions of Windows, the default pool is used.</span></span>
    -   <span data-ttu-id="c9ad3-121">Wenn \_ RpcMgmtEnableDedicatedThreadPool aufgerufen wird, bevor eine RPC-API aufgerufen wird, wird der private Thread Pool verwendet (Vista-Verhalten).</span><span class="sxs-lookup"><span data-stu-id="c9ad3-121">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior).</span></span>
    -   <span data-ttu-id="c9ad3-122">Wenn ich \_ RpcMgmtEnableDedicatedThreadPool nach einem RPC-Aufruf aufgerufen wird, wird der Standard Pool verwendet \_ . i RpcMgmtEnableDedicatedThreadPool gibt den Fehler 1764 zurück, und der angeforderte Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-122">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported.</span></span>

-   <span data-ttu-id="c9ad3-123">Windows Vista (Standard): für Binärdateien, die für Windows Vista und frühere Versionen von Windows kompiliert wurden, wird der private Pool verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-123">Windows Vista (default): For binaries compiled for Windows Vista and earlier versions of Windows, the private pool is used.</span></span>

<span data-ttu-id="c9ad3-124">**DirectDraw-Sperre**</span><span class="sxs-lookup"><span data-stu-id="c9ad3-124">**DirectDraw lock**</span></span>

-   <span data-ttu-id="c9ad3-125">Windows 8 und Windows 7: für Windows 7 und höhere Versionen des Betriebssystems manifestierte Apps können die Lock-API in ddraw nicht aufrufen, um den primären Desktop-Video Puffer zu sperren. Dies führt zu einem Fehler, und es wird ein NULL-Zeiger für das primäre Replikat zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-125">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of the operating system cannot call Lock API in DDRAW to lock the primary desktop video buffer; doing so will result in an error, and a NULL pointer for the primary is returned.</span></span> <span data-ttu-id="c9ad3-126">Dieses Verhalten wird auch dann erzwungen, wenn Desktopfenster-Manager Komposition nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-126">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="c9ad3-127">Apps, deren Kompatibilität für Windows 7 und höher deklariert wurde, dürfen den primären Video Puffer nicht zum renderingsperren sperren.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-127">Apps with compatibility declared for Windows 7 and later must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="c9ad3-128">Windows Vista (Standard): Apps können eine Sperre für den primären Video Puffer erhalten, da ältere apps von diesem Verhalten abhängig sind. Wenn Sie die app ausführen, wird Desktopfenster-Manager deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-128">Windows Vista (default): Apps can acquire a lock on the primary video buffer, as legacy apps depend on this behavior; running the app turns off Desktop Window Manager.</span></span>

<span data-ttu-id="c9ad3-129">**DirectDraw-Bitblock Übertragung (BitBLT) zum primären Replikat ohne Clipping-Fenster**</span><span class="sxs-lookup"><span data-stu-id="c9ad3-129">**DirectDraw bit-block transfer (bitblt) to primary without clipping window**</span></span>

-   <span data-ttu-id="c9ad3-130">Windows 8 und Windows 7: für Windows 7 und höhere Versionen von Windows dargestellte apps werden daran gehindert, ein BitBlt für den primären Desktop-Video Puffer ohne clippingfenster auszuführen. Dies führt zu einem Fehler, und der BitBLT-Bereich wird nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-130">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of Windows are prevented from performing a bitblt to the primary Desktop video buffer without a clipping window; doing so results in an error and the bitblt area will not be rendered.</span></span> <span data-ttu-id="c9ad3-131">Windows erzwingt dieses Verhalten auch dann, wenn Sie Desktopfenster-Manager Komposition nicht aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-131">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="c9ad3-132">Apps, deren Kompatibilität für Windows 7 und höher deklariert wurde, müssen ein BitBLT in einem clippingfenster ausführen.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-132">Apps with compatibility declared for Windows 7 and later must perform a bitblt to a clipping window.</span></span>
-   <span data-ttu-id="c9ad3-133">Windows Vista (Standard): apps müssen in der Lage sein, ein BitBLT-Element ohne clippingfenster auf das primäre Replikat auszuführen, da Legacy-apps von diesem Verhalten abhängig sind. Wenn Sie diese APP ausführen, wird die Desktopfenster-Manager deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-133">Windows Vista (default): Apps must be able to perform a bitblt to the primary without a clipping window, as legacy apps depend on this behavior; running this app turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="c9ad3-134">**Ge-verlappedresult-API**</span><span class="sxs-lookup"><span data-stu-id="c9ad3-134">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="c9ad3-135">Windows 8 und Windows 7: löst eine Racebedingung aus, bei der eine Multithread-APP, die **gedeverlappedresult** verwendet, zurückgeben kann, ohne das Ereignis in der überlappenden Struktur zurückzusetzen. Dadurch wird der nächste Aufrufe dieser Funktion vorzeitig zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-135">Windows 8 and Windows 7: Resolves a race condition where a multithreaded app using **GetOverlappedResult** can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="c9ad3-136">Windows Vista (Standard): stellt das Verhalten mit der Racebedingung bereit, von der Apps möglicherweise abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-136">Windows Vista (default): Provides the behavior with the race condition that apps might have a dependency on.</span></span> <span data-ttu-id="c9ad3-137">Apps, die dieses Race vor dem Windows 7-Verhalten vermeiden müssen, sollten auf das überlappende Ereignis warten und bei Signalisierung gedeverlappedresult mit bwait = = false aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-137">Apps that must avoid this race prior to the Windows 7 behavior should wait on the overlapped event and, when signaled, call GetOverlappedResult with bWait == FALSE.</span></span>

<span data-ttu-id="c9ad3-138">**Status von shelldesigns im Modus mit hohem Kontrast**</span><span class="sxs-lookup"><span data-stu-id="c9ad3-138">**Shell themes status in high contrast mode**</span></span>

-   <span data-ttu-id="c9ad3-139">Windows 8: gibt den tatsächlichen Themenstatus für im Modus mit hohem Kontrast zurück.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-139">Windows 8: Returns the real theming status for when in high contrast mode.</span></span>
-   <span data-ttu-id="c9ad3-140">Windows 7: gibt das Design im Modus mit hohem Kontrast als nicht verfügbar zurück, da DWM noch immer eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-140">Windows 7: Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>
-   <span data-ttu-id="c9ad3-141">Windows Vista (Standard): gibt das Design im Modus mit hohem Kontrast als nicht verfügbar zurück, da DWM noch immer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-141">Windows Vista (default): Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>

<span data-ttu-id="c9ad3-142">**Shell IPersistFile:: Save-Methode**</span><span class="sxs-lookup"><span data-stu-id="c9ad3-142">**Shell iPersistFile::Save method**</span></span>

-   <span data-ttu-id="c9ad3-143">Windows 8: cshelllink:: Save bestimmt jetzt, ob der IPersistFile-Handler mit einem relativen Pfad Argument aufgerufen wird, und schlägt den Aufruf fehl, wenn dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-143">Windows 8: CShellLink::Save now determines if the IPersistFile handler is called with a relative path argument and fails the call if it is.</span></span>

    <span data-ttu-id="c9ad3-144">Die [öffentliche Dokumentation](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , die dieses Verhalten beschreibt, gibt an, dass das Pfad Argument ein absoluter Pfad sein muss:</span><span class="sxs-lookup"><span data-stu-id="c9ad3-144">The [public documentation](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) describing this behavior indicates that path argument has to be an absolute path:</span></span>

-   <span data-ttu-id="c9ad3-145">Windows 7 und früher (Standard): cshelllink:: Save bestimmt nicht, ob der IPersistFile-Handler eine relative Pfad Überprüfung sendet und ermöglicht, dass apps weiterhin mit absoluten oder relativen Pfaden arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-145">Windows 7 and earlier (default): CShellLink::Save does not determine if the iPersistFile handler sends a relative path check and allows apps to continue working with absolute or relative paths.</span></span>

<span data-ttu-id="c9ad3-146">**Programmkompatibilitäts-Assistent (PCA)**</span><span class="sxs-lookup"><span data-stu-id="c9ad3-146">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="c9ad3-147">Windows 8: apps mit dem Kompatibilitäts Abschnitt erhalten keine PCA-Entschärfung.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-147">Windows 8: Apps with the compatibility section do not get the PCA mitigation.</span></span>
-   <span data-ttu-id="c9ad3-148">Windows 7: apps mit dem Kompatibilitäts Abschnitt werden auf mögliche Kompatibilitätsprobleme bei Windows 8-Änderungen nachverfolgt (in diesem Dokument beschrieben).</span><span class="sxs-lookup"><span data-stu-id="c9ad3-148">Windows 7: Apps with the compatibility section are tracked for potential compatibility issues for Windows 8 changes (described in this document).</span></span>
-   <span data-ttu-id="c9ad3-149">Windows Vista (Standard): apps, die in bestimmten Situationen nicht ordnungsgemäß installiert werden oder während der Laufzeit abstürzen, erhalten die PCA-Entschärfung.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-149">Windows Vista (default): Apps that fail to install properly or crash during runtime under some specific circumstances get the PCA mitigation.</span></span> <span data-ttu-id="c9ad3-150">Weitere Informationen finden Sie im Abschnitt "Resources" (Ressourcen).</span><span class="sxs-lookup"><span data-stu-id="c9ad3-150">For more info, see the Resources section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="c9ad3-151">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="c9ad3-151">Leveraging feature capabilities</span></span>

<span data-ttu-id="c9ad3-152">Aktualisieren Sie das App-Manifest mit den neuesten Kompatibilitätsinformationen für die Betriebssystemunterstützung.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-152">Update the app manifest with the latest compatibility info for operating system support.</span></span> <span data-ttu-id="c9ad3-153">In diesem Abschnitt werden die Ergänzungen des Manifests beschrieben:</span><span class="sxs-lookup"><span data-stu-id="c9ad3-153">This section describes the additions to the manifest:</span></span>

<span data-ttu-id="c9ad3-154">**Namespace:** Compatibility. v1 (xmlns = "urn: Schemas-Microsoft-com: Compatibility. v1" >)</span><span class="sxs-lookup"><span data-stu-id="c9ad3-154">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

<span data-ttu-id="c9ad3-155">**Abschnitts Name:** Kompatibilität (neuer Abschnitt)</span><span class="sxs-lookup"><span data-stu-id="c9ad3-155">**Section name:** Compatibility (new section)</span></span>

<span data-ttu-id="c9ad3-156">**SupportedOS:** GUID des unterstützten Betriebssystems: die GUIDs, die den unterstützten Betriebssystemen zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="c9ad3-156">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

-   <span data-ttu-id="c9ad3-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="c9ad3-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span>

    <span data-ttu-id="c9ad3-158">für **Windows Vista**: Dies ist der Standardwert für den switchbackkontext.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-158">for **Windows Vista**: This is the default value for the switchback context</span></span>

-   <span data-ttu-id="c9ad3-159">{35138b9a-5d96-4f BD-8e2d-a2440225b93a}</span><span class="sxs-lookup"><span data-stu-id="c9ad3-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span>

    <span data-ttu-id="c9ad3-160">für **Windows 7**: apps, die diesen Wert im App-Manifest festlegen, erhalten das Windows 7-Verhalten.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-160">for **Windows 7**: Apps that set this value in the app manifest get the Windows 7 behavior</span></span>

-   <span data-ttu-id="c9ad3-161">{4a2b28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="c9ad3-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span>

    <span data-ttu-id="c9ad3-162">für **Windows 8**: apps, die diesen Wert im Anwendungs Manifest festlegen, erhalten das Windows 8-Verhalten.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-162">for **Windows 8**: Apps that set this value in the application manifest get the Windows 8 behavior</span></span>

<span data-ttu-id="c9ad3-163">Microsoft generiert und veröffentlicht GUIDs für zukünftige Windows-Versionen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-163">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

<span data-ttu-id="c9ad3-164">Ein XML-Beispiel für ein aktualisiertes Manifest:</span><span class="sxs-lookup"><span data-stu-id="c9ad3-164">An XML example of an updated manifest:</span></span>

> [!Note]  
> <span data-ttu-id="c9ad3-165">Beim Attribut-und Tagnamen im App-Manifest wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-165">The attribute and tag names in the app manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



<span data-ttu-id="c9ad3-166">Die GUIDs für alle Betriebssysteme im vorherigen Beispiel bieten Unterstützung auf der Basis von.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-166">The GUIDs for all the operating systems in the previous example provide down-level support.</span></span> <span data-ttu-id="c9ad3-167">Apps, die mehrere Plattformen unterstützen, benötigen für jede Plattform keine separaten Manifeste.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-167">Apps that support multiple platforms do not need separate manifests for each platform.</span></span>

## <a name="tests"></a><span data-ttu-id="c9ad3-168">Tests</span><span class="sxs-lookup"><span data-stu-id="c9ad3-168">Tests</span></span>

<span data-ttu-id="c9ad3-169">Eine APP kann mehrere unterstützte Betriebssystem-IDs angeben.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-169">An app can specify multiple supported operating system IDs.</span></span> <span data-ttu-id="c9ad3-170">Sie sollten eine unterstützte Betriebssystem-ID hinzufügen, wenn Sie die APP auf diesem Betriebssystem getestet oder getestet haben.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-170">You should add a supported operating system ID if you have tested, or are in the process of testing, the app on that operating system.</span></span> <span data-ttu-id="c9ad3-171">Diese Einträge werden von Windows Vista und früheren Betriebssystemversionen nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-171">Windows Vista and prior operating system versions do not pay attention to these entries.</span></span> <span data-ttu-id="c9ad3-172">Ab Windows 7 wählt Windows die höchste Versions-GUID im Manifest bis zur laufenden Windows-Version aus und unterstützt die APP auf dieser Ebene.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-172">Starting with Windows 7, Windows will choose the highest version GUID in the manifest up to the running Windows version, and give the app support at that level.</span></span> <span data-ttu-id="c9ad3-173">So überprüfen Sie, ob die APP mit dem neuen Kompatibilitäts Abschnitt des App-Manifests funktioniert:</span><span class="sxs-lookup"><span data-stu-id="c9ad3-173">To verify that the app works with the new app manifest compatibility section:</span></span>

1.  <span data-ttu-id="c9ad3-174">Testen Sie die APP mit dem neuen Kompatibilitäts Abschnitt und SupportedOS ID = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}, um sicherzustellen, dass die APP mit dem aktuellen Windows 8-Verhalten ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-174">Test the app with the new compatibility section and SupportedOS ID = { 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} to ensure that the app works properly using the latest Windows 8 behavior.</span></span>
2.  <span data-ttu-id="c9ad3-175">Testen Sie die APP mit dem neuen Kompatibilitäts Abschnitt und SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a}, um sicherzustellen, dass die APP unter Verwendung des Windows 7-Verhaltens ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-175">Test the app with the new compatibility section and SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} to ensure that the app works properly using the Windows 7 behavior.</span></span>
3.  <span data-ttu-id="c9ad3-176">Testen Sie die APP mit dem neuen Kompatibilitäts Abschnitt und SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0}, um sicherzustellen, dass die APP mit dem Windows Vista-Verhalten ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c9ad3-176">Test the app with the new compatibility section and SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0} to ensure that the app works properly using the Windows Vista behavior.</span></span>

## <a name="resources"></a><span data-ttu-id="c9ad3-177">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c9ad3-177">Resources</span></span>

-   [<span data-ttu-id="c9ad3-178">Queryactctxw-Funktion</span><span class="sxs-lookup"><span data-stu-id="c9ad3-178">QueryActCtxW Function</span></span>](../sbscs/application-manifests.md)
-   <span data-ttu-id="c9ad3-179">[UAC-Manifest](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c9ad3-179">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="c9ad3-180">Anwendungs Manifeste für Windows-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c9ad3-180">Application Manifests for Windows Applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="c9ad3-181">Desktopfenster-Manager (DWM)</span><span class="sxs-lookup"><span data-stu-id="c9ad3-181">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="c9ad3-182">Aktualisierung des Kontext Konflikts</span><span class="sxs-lookup"><span data-stu-id="c9ad3-182">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)
-   <span data-ttu-id="c9ad3-183">[Programmkompatibilitäts-Assistent](/previous-versions/bb756937(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c9ad3-183">[Program Compatibility Assistant](/previous-versions/bb756937(v=msdn.10))</span></span>

 

 