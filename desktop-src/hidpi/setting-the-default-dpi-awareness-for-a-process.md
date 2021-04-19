---
description: 'Weitere Informationen finden Sie unter: Festlegen der standardmäßigen dpi-Informationen für einen Prozess'
title: Festlegen der Standard-dpi-Informationen für einen Prozess (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: ff869974e6d9aa2eec2b3251832c061d7b6826da
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106366383"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a><span data-ttu-id="6dec1-103">Festlegen der Standard-dpi-Informationen für einen Prozess</span><span class="sxs-lookup"><span data-stu-id="6dec1-103">Setting the default DPI awareness for a process</span></span>

<span data-ttu-id="6dec1-104">Desktop Anwendungen unter Windows können in unterschiedlichen dpi-Methoden ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6dec1-104">Desktop applications on Windows can run in different DPI awareness modes.</span></span> <span data-ttu-id="6dec1-105">Diese Modi ermöglichen verschiedene dpi-Skalierungs Verhalten und können unterschiedliche Koordinaten Bereiche verwenden.</span><span class="sxs-lookup"><span data-stu-id="6dec1-105">These modes enable different DPI scaling behavior and can use different coordinate spaces.</span></span> <span data-ttu-id="6dec1-106">Weitere Informationen zu dpi-Informationen finden Sie unter [hohe dpi-Entwicklung für Desktop Anwendungen unter Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="6dec1-106">For more information on DPI awareness, see [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span></span> <span data-ttu-id="6dec1-107">Es ist wichtig, dass Sie den standardmäßigen dpi-Informationsmodus des Prozesses explizit festlegen, um unerwartetes Verhalten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6dec1-107">It is important that you explicitly set the default DPI awareness mode of your process so as to avoid unexpected behavior.</span></span>

<span data-ttu-id="6dec1-108">Es gibt zwei Hauptmethoden, um das standardmäßige dpi-Bewusstsein eines Prozesses anzugeben:</span><span class="sxs-lookup"><span data-stu-id="6dec1-108">There are two main methods to specify the default DPI awareness of a process:</span></span>

<span data-ttu-id="6dec1-109">1 \) durch eine Einstellung für das Anwendungs Manifest</span><span class="sxs-lookup"><span data-stu-id="6dec1-109">1\) through an application manifest setting</span></span>

<span data-ttu-id="6dec1-110">2 Programm gesteuertes ausführen \) eines API-Aufrufes</span><span class="sxs-lookup"><span data-stu-id="6dec1-110">2\) programmatically through an API call</span></span>

<span data-ttu-id="6dec1-111">Es wird empfohlen, dass Sie den Standardprozess-dpi-Wert über eine Manifest-Einstellung angeben.</span><span class="sxs-lookup"><span data-stu-id="6dec1-111">We recommended that you specify the default process DPI awareness via a manifest setting.</span></span> <span data-ttu-id="6dec1-112">Die Angabe der standardmäßigen via-API wird zwar unterstützt, es wird jedoch nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="6dec1-112">While specifying the default via API is supported, it is not recommended.</span></span>

## <a name="setting-default-awareness-with-the-application-manifest"></a><span data-ttu-id="6dec1-113">Festlegen von Standard Bekanntheit mit dem Anwendungs Manifest</span><span class="sxs-lookup"><span data-stu-id="6dec1-113">Setting default awareness with the application manifest</span></span>

<span data-ttu-id="6dec1-114">Es gibt zwei Manifest-Einstellungen, mit denen Sie den Prozessstandard-dpi-Awareness-Modus angeben können: \<dpiAwareness\> und \<dpiAware\> .</span><span class="sxs-lookup"><span data-stu-id="6dec1-114">There are two manifest settings that enable you to specify the process default DPI awareness mode: \<dpiAwareness\> and \<dpiAware\>.</span></span> <span data-ttu-id="6dec1-115">\<dpiAware\> wurde in Windows Vista eingeführt und ermöglicht nur, dass Ihr ProzessStandard mäßig auf System Bewusstsein festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6dec1-115">\<dpiAware\> was introduced in Windows Vista and only enables your process default to be set to system awareness.</span></span> <span data-ttu-id="6dec1-116">\<dpiAwareness\> wurde in Windows 10, Version 1607, eingeführt und ermöglicht Ihnen das Angeben einer geordneten Liste von Prozess-Standard-dpi-Informations Modi.</span><span class="sxs-lookup"><span data-stu-id="6dec1-116">\<dpiAwareness\> was introduced in Windows 10, version 1607 and enables you to specify an ordered list of process-default DPI awareness modes.</span></span> <span data-ttu-id="6dec1-117">Dies ermöglicht es Ihnen, die Kompatibilitäts Modi für die Sicherung festzulegen, die verwendet werden, wenn Ihre Anwendung auf einer Version von Windows ausgeführt wird und den ersten angegebenen Informationsmodus nicht unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="6dec1-117">This enables you to set backup DPI awareness modes, which will be used if your application is ran on a version of Windows unable to support the first awareness mode specified.</span></span> <span data-ttu-id="6dec1-118">In älteren Versionen von Windows wird das neuere \<dpiAwareness\> Tag ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6dec1-118">On older versions of Windows, the newer \<dpiAwareness\> tag will be ignored.</span></span> <span data-ttu-id="6dec1-119">Dies bedeutet, dass Sie beide Manifest-Einstellungen verwenden können, um ein Szenario zu aktivieren, bei dem der ProzessStandard bei der Per-Monitor unter Windows 10, Version 1607, Systeminformationen für ältere Windows-Versionen ist.</span><span class="sxs-lookup"><span data-stu-id="6dec1-119">This means that you can use both of these manifest settings to enable a scenario where your process default could be system awareness on older version of Windows while being Per-Monitor on versions greater than Windows 10, version 1607.</span></span> <span data-ttu-id="6dec1-120">Unter Windows 10, Version 1607 und auf, wird die \<dpiAware\> Einstellung ignoriert, wenn das \<dpiAwareness\> Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6dec1-120">On Windows 10, version 1607, and on, the \<dpiAware\> setting is ignored if the \<dpiAwareness\> element is present.</span></span>

<span data-ttu-id="6dec1-121">In der folgenden Tabelle wird gezeigt, wie verschiedene ProzessStandard-dpi-Informations Modi mithilfe der beiden Manifest-Einstellungen angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6dec1-121">The table below shows how to specify different process-default DPI awareness modes using the two manifest settings:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dec1-122">Standard-dpi-Modus verarbeiten</span><span class="sxs-lookup"><span data-stu-id="6dec1-122">Process default DPI awareness mode</span></span></th>
<th><span data-ttu-id="6dec1-123">&lt;dpiaware- &gt; Einstellung</span><span class="sxs-lookup"><span data-stu-id="6dec1-123">&lt;dpiAware&gt; setting</span></span></th>
<th><span data-ttu-id="6dec1-124">&lt;dpiawareness &gt; -Einstellung (Windows 10, Version 1607 und höher)</span><span class="sxs-lookup"><span data-stu-id="6dec1-124">&lt;dpiAwareness&gt; setting (Windows 10, version 1607 and later)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dec1-125">bewusste</span><span class="sxs-lookup"><span data-stu-id="6dec1-125">unaware</span></span></td>
<td><p><span data-ttu-id="6dec1-126">N/v (keine dpiaware-Einstellung im Manifest)</span><span class="sxs-lookup"><span data-stu-id="6dec1-126">N/A (no dpiAware setting in manifest)</span></span></p>
<p><span data-ttu-id="6dec1-127">oder</span><span class="sxs-lookup"><span data-stu-id="6dec1-127">or</span></span></p>
<p><span data-ttu-id="6dec1-128">&lt;dpiaware &gt; false &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="6dec1-128">&lt;dpiAware&gt;false&lt;/dpiAware&gt;</span></span></p></td>
<td><span data-ttu-id="6dec1-129">&lt;dpiawareness ist &gt; nicht bekannt &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="6dec1-129">&lt;dpiAwareness&gt;unaware&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dec1-130">System fähig</span><span class="sxs-lookup"><span data-stu-id="6dec1-130">System aware</span></span></td>
<td><span data-ttu-id="6dec1-131">&lt;dpiaware &gt; true &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="6dec1-131">&lt;dpiAware&gt;true&lt;/dpiAware&gt;</span></span></td>
<td><span data-ttu-id="6dec1-132">&lt;dpiawareness- &gt; System &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="6dec1-132">&lt;dpiAwareness&gt;system&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dec1-133">Pro Monitor</span><span class="sxs-lookup"><span data-stu-id="6dec1-133">Per Monitor</span></span></td>
<td><span data-ttu-id="6dec1-134">&lt;dpiaware &gt; true/PM &lt; dpiaware&gt;</span><span class="sxs-lookup"><span data-stu-id="6dec1-134">&lt;dpiAware&gt;true/pm&lt;dpiAware&gt;</span></span></td>
<td><span data-ttu-id="6dec1-135">&lt;dpiawareness &gt; permonitor &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="6dec1-135">&lt;dpiAwareness&gt;PerMonitor&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dec1-136">Pro Monitor v2</span><span class="sxs-lookup"><span data-stu-id="6dec1-136">Per Monitor V2</span></span></td>
<td><span data-ttu-id="6dec1-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6dec1-137">Not supported</span></span></td>
<td><span data-ttu-id="6dec1-138">&lt;dpiawareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="6dec1-138">&lt;dpiAwareness&gt;PerMonitorV2&lt;/dpiAwareness&gt;</span></span></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6dec1-139">Das folgende Beispiel zeigt sowohl die \<dpiAwareness\> -als auch die-Einstellungen, die \<dpiAware\> in derselben Manifest-Datei verwendet werden, um das Prozess-Standardverhalten des dpi-Manifests für verschiedene Versionen von Windows zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6dec1-139">The sample below shows both the \<dpiAwareness\> and the \<dpiAware\> settings being used within the same manifest file to configure process-default DPI awareness behavior for different versions of Windows.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
  <asmv3:application>
    <asmv3:windowsSettings>
      <dpiAware xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">true</dpiAware>
      <dpiAwareness xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">PerMonitorV2</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

## <a name="setting-default-awareness-programmatically"></a><span data-ttu-id="6dec1-140">Programm gesteuertes Festlegen von Standardinformationen</span><span class="sxs-lookup"><span data-stu-id="6dec1-140">Setting default awareness programmatically</span></span>

<span data-ttu-id="6dec1-141">Obwohl es nicht empfohlen wird, ist es möglich, das standardmäßige dpi-Bewusstsein Programm gesteuert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6dec1-141">Although it is not recommended, it is possible to set the default DPI awareness programmatically.</span></span> <span data-ttu-id="6dec1-142">Sobald ein Fenster (ein HWND) in Ihrem Prozess erstellt wurde, wird das Ändern des dpi-Informationsmodus nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6dec1-142">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="6dec1-143">Wenn Sie den Prozess-Standard-dpi-Informationsmodus Programm gesteuert festlegen, müssen Sie die entsprechende API vor dem Erstellen von HWNDs aufruft.</span><span class="sxs-lookup"><span data-stu-id="6dec1-143">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span>

<span data-ttu-id="6dec1-144">Es gibt mehrere APIs, mit denen Sie das standardmäßige dpi-Bewusstsein für Ihren Prozess angeben können.</span><span class="sxs-lookup"><span data-stu-id="6dec1-144">There are multiple APIs that let you specify the default DPI awareness for your process.</span></span> <span data-ttu-id="6dec1-145">Die aktuelle empfohlene API ist " [**setprocessdpiawarsess Context**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))", da ältere APIs weniger Funktionen bieten.</span><span class="sxs-lookup"><span data-stu-id="6dec1-145">The current recommended API is [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), as older APIs offer less functionality.</span></span>

 

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6dec1-146">API</span><span class="sxs-lookup"><span data-stu-id="6dec1-146">API</span></span></th>
<th><span data-ttu-id="6dec1-147">Mindestversion von Windows</span><span class="sxs-lookup"><span data-stu-id="6dec1-147">Minimum version of Windows</span></span></th>
<th><span data-ttu-id="6dec1-148">DPI nicht bekannt</span><span class="sxs-lookup"><span data-stu-id="6dec1-148">DPI Unaware</span></span></th>
<th><span data-ttu-id="6dec1-149">System-dpi-fähig</span><span class="sxs-lookup"><span data-stu-id="6dec1-149">System DPI Aware</span></span></th>
<th><span data-ttu-id="6dec1-150">DPI-Erkennung pro Monitor</span><span class="sxs-lookup"><span data-stu-id="6dec1-150">Per Monitor DPI Aware</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6dec1-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></span><span class="sxs-lookup"><span data-stu-id="6dec1-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></span></span></td>
<td><span data-ttu-id="6dec1-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6dec1-152">Windows Vista</span></span></td>
<td><span data-ttu-id="6dec1-153">–</span><span class="sxs-lookup"><span data-stu-id="6dec1-153">N/A</span></span></td>
<td><span data-ttu-id="6dec1-154">SetProcessDPIAware ()</span><span class="sxs-lookup"><span data-stu-id="6dec1-154">SetProcessDpiAware()</span></span></td>
<td><span data-ttu-id="6dec1-155">–</span><span class="sxs-lookup"><span data-stu-id="6dec1-155">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6dec1-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>Setprocessdpiawareness</strong></a></span><span class="sxs-lookup"><span data-stu-id="6dec1-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span></span></td>
<td><span data-ttu-id="6dec1-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6dec1-157">Windows 8.1</span></span></td>
<td><span data-ttu-id="6dec1-158">Setprocessdpiawareness (PROCESS_DPI_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="6dec1-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span></span></td>
<td><span data-ttu-id="6dec1-159">Setprocessdpiawareness (PROCESS_DPI_SYSTEM_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="6dec1-159">SetProcessDpiAwareness(PROCESS_DPI_SYSTEM_DPI_AWARE)</span></span></td>
<td><span data-ttu-id="6dec1-160">Setprocessdpiawareness (PROCESS_DPI_PER_MONITOR_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="6dec1-160">SetProcessDpiAwareness(PROCESS_DPI_PER_MONITOR_DPI_AWARE)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6dec1-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>Setprocessdpiawareress Context</strong></a></span><span class="sxs-lookup"><span data-stu-id="6dec1-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span></span></td>
<td><span data-ttu-id="6dec1-162">Windows 10, Version 1607</span><span class="sxs-lookup"><span data-stu-id="6dec1-162">Windows 10, version 1607</span></span></td>
<td><span data-ttu-id="6dec1-163">Setprocessdpiawareress Context (DPI_AWARENESS_CONTEXT_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="6dec1-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span></span></td>
<td><span data-ttu-id="6dec1-164">Setprocessdpiawareress Context (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span><span class="sxs-lookup"><span data-stu-id="6dec1-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span></span></td>
<td><p><span data-ttu-id="6dec1-165">Setprocessdpiawareress Context (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span><span class="sxs-lookup"><span data-stu-id="6dec1-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span></span></p>
<p><span data-ttu-id="6dec1-166">Setprocessdpiawareress Context (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span><span class="sxs-lookup"><span data-stu-id="6dec1-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a><span data-ttu-id="6dec1-167">Prozess-Standard Vergleich und Thread Standard</span><span class="sxs-lookup"><span data-stu-id="6dec1-167">Process-default vs. Thread default</span></span>

<span data-ttu-id="6dec1-168">Dieses Dokument bezieht sich auf das Festlegen der Standard-dpi-Informationen für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6dec1-168">This document refers to setting the default DPI awareness for your process.</span></span> <span data-ttu-id="6dec1-169">Dies liegt daran, dass Windows 10 die Unterstützung für die Ausführung von mehr als einem dpi-Modus in einem einzelnen Prozess (vor Windows 10) eingeführt hat (vor Windows 10 musste der gesamte Prozess einem einzigen dpi-Awareness-Modus entsprechen).</span><span class="sxs-lookup"><span data-stu-id="6dec1-169">This is because Windows 10 introduced support for running more than one DPI awareness mode within a single process (prior to Windows 10, the entire process had to conform to a single DPI awareness mode).</span></span> <span data-ttu-id="6dec1-170">Die Unterstützung für das Ausführen von mehr als einem dpi-Informationsmodus innerhalb eines Prozesses wird als "DPI-Skalierung im gemischten Modus" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6dec1-170">Support for running more than one DPI awareness mode within a process is referred to as "mixed-mode DPI scaling".</span></span> <span data-ttu-id="6dec1-171">Wenn Sie die DPI-Skalierung im gemischten Modus innerhalb des Prozesses verwenden, kann jedes Fenster der obersten Ebene in einem dpi-Modus ausgeführt werden, der sich von der Standardeinstellung des Prozesses unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="6dec1-171">When using mixed-mode DPI scaling within your process, each top-level Window can run in a DPI awareness mode that may be different than that of the process default.</span></span> <span data-ttu-id="6dec1-172">Sofern nicht explizit angegeben, wird jeder Thread bei der Erstellung standardmäßig auf den Standardprozess eingestellt.</span><span class="sxs-lookup"><span data-stu-id="6dec1-172">Unless explicitly specified, each thread will default to the process default when created.</span></span> <span data-ttu-id="6dec1-173">Weitere Informationen zur DPI-Skalierung im gemischten Modus finden Sie im Artikel zur [DPI-Skalierung im gemischten Modus](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .</span><span class="sxs-lookup"><span data-stu-id="6dec1-173">For more information about mixed-mode DPI scaling, refer to the [Mixed-Mode DPI Scaling](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) article.</span></span>
