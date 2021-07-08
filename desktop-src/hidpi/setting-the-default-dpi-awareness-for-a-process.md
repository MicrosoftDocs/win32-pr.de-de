---
description: Weitere Informationen finden Sie unter Festlegen des DPI-Standardbewusstseins für einen Prozess.
title: Festlegen des DPI-Standardbewusstseins für einen Prozess (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: c9192bf650588b7c21f17afb45149fe460f91bea
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481865"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a><span data-ttu-id="831d9-103">Festlegen des DPI-Standardbewusstseins für einen Prozess</span><span class="sxs-lookup"><span data-stu-id="831d9-103">Setting the default DPI awareness for a process</span></span>

<span data-ttu-id="831d9-104">Desktopanwendungen auf Windows können in verschiedenen DPI-Bewusstseinsmodi ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="831d9-104">Desktop applications on Windows can run in different DPI awareness modes.</span></span> <span data-ttu-id="831d9-105">Diese Modi ermöglichen ein anderes DPI-Skalierungsverhalten und können unterschiedliche Koordinatenräume verwenden.</span><span class="sxs-lookup"><span data-stu-id="831d9-105">These modes enable different DPI scaling behavior and can use different coordinate spaces.</span></span> <span data-ttu-id="831d9-106">Weitere Informationen zur DPI-Bekanntheit finden Sie unter [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="831d9-106">For more information on DPI awareness, see [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span></span> <span data-ttu-id="831d9-107">Es ist wichtig, dass Sie explizit den standardmäßigen DPI-Bewusstseinsmodus Ihres Prozesses festlegen, um unerwartetes Verhalten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="831d9-107">It is important that you explicitly set the default DPI awareness mode of your process so as to avoid unexpected behavior.</span></span>

<span data-ttu-id="831d9-108">Es gibt zwei Hauptmethoden, um die Standard-DPI-Kenntnis eines Prozesses anzugeben:</span><span class="sxs-lookup"><span data-stu-id="831d9-108">There are two main methods to specify the default DPI awareness of a process:</span></span>

<span data-ttu-id="831d9-109">1 \) bis zu einer Anwendungsmanifesteinstellung</span><span class="sxs-lookup"><span data-stu-id="831d9-109">1\) through an application manifest setting</span></span>

<span data-ttu-id="831d9-110">2 \) programmgesteuert über einen API-Aufruf</span><span class="sxs-lookup"><span data-stu-id="831d9-110">2\) programmatically through an API call</span></span>

<span data-ttu-id="831d9-111">Es wird empfohlen, den DPI-Standardprozess über eine Manifesteinstellung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="831d9-111">We recommended that you specify the default process DPI awareness via a manifest setting.</span></span> <span data-ttu-id="831d9-112">Die Angabe des Standardwerts über die API wird zwar unterstützt, wird jedoch nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="831d9-112">While specifying the default via API is supported, it is not recommended.</span></span>

## <a name="setting-default-awareness-with-the-application-manifest"></a><span data-ttu-id="831d9-113">Festlegen des Standardbewusstseins mit dem Anwendungsmanifest</span><span class="sxs-lookup"><span data-stu-id="831d9-113">Setting default awareness with the application manifest</span></span>

<span data-ttu-id="831d9-114">Es gibt zwei Manifesteinstellungen, mit denen Sie den Standardmäßigen DPI-Aktivierungsmodus des Prozesses angeben können: \<dpiAwareness\> und \<dpiAware\> .</span><span class="sxs-lookup"><span data-stu-id="831d9-114">There are two manifest settings that enable you to specify the process default DPI awareness mode: \<dpiAwareness\> and \<dpiAware\>.</span></span> <span data-ttu-id="831d9-115">\<dpiAware\>wurde in Windows Vista eingeführt und ermöglicht nur, dass Ihr Prozess standardmäßig auf Systembewusstsein festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="831d9-115">\<dpiAware\> was introduced in Windows Vista and only enables your process default to be set to system awareness.</span></span> <span data-ttu-id="831d9-116">\<dpiAwareness\>wurde in Windows 10 Version 1607 eingeführt und ermöglicht ihnen das Angeben einer geordneten Liste von prozessbasierten DPI-Awareness-Modi.</span><span class="sxs-lookup"><span data-stu-id="831d9-116">\<dpiAwareness\> was introduced in Windows 10, version 1607 and enables you to specify an ordered list of process-default DPI awareness modes.</span></span> <span data-ttu-id="831d9-117">Dadurch können Sie Sicherungs-DPI-Awareness-Modi festlegen, die verwendet werden, wenn Ihre Anwendung auf einer Version von ausgeführt wird, Windows den ersten angegebenen Bewusstseinsmodus nicht unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="831d9-117">This enables you to set backup DPI awareness modes, which will be used if your application is ran on a version of Windows unable to support the first awareness mode specified.</span></span> <span data-ttu-id="831d9-118">Bei älteren Windows wird das neuere Tag \<dpiAwareness\> ignoriert.</span><span class="sxs-lookup"><span data-stu-id="831d9-118">On older versions of Windows, the newer \<dpiAwareness\> tag will be ignored.</span></span> <span data-ttu-id="831d9-119">Dies bedeutet, dass Sie beide Manifesteinstellungen verwenden können, um ein Szenario zu ermöglichen, in dem Ihre Prozesseinstellung auf ältere Versionen von Windows festgelegt werden kann, während sie Per-Monitor für Versionen größer als Windows 10, Version 1607, verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="831d9-119">This means that you can use both of these manifest settings to enable a scenario where your process default could be system awareness on older version of Windows while being Per-Monitor on versions greater than Windows 10, version 1607.</span></span> <span data-ttu-id="831d9-120">In Windows 10 Version 1607 und on wird die Einstellung \<dpiAware\> ignoriert, wenn \<dpiAwareness\> das Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="831d9-120">On Windows 10, version 1607, and on, the \<dpiAware\> setting is ignored if the \<dpiAwareness\> element is present.</span></span>

<span data-ttu-id="831d9-121">In der folgenden Tabelle wird gezeigt, wie sie mithilfe der beiden Manifesteinstellungen unterschiedliche Prozess-Standard-DPI-Bewusstseinsmodi angeben:</span><span class="sxs-lookup"><span data-stu-id="831d9-121">The table below shows how to specify different process-default DPI awareness modes using the two manifest settings:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="831d9-122">Verarbeiten des standardmäßigen DPI-Bewusstseinsmodus</span><span class="sxs-lookup"><span data-stu-id="831d9-122">Process default DPI awareness mode</span></span></th>
<th><span data-ttu-id="831d9-123">&lt;dpiAware-Einstellung &gt;</span><span class="sxs-lookup"><span data-stu-id="831d9-123">&lt;dpiAware&gt; setting</span></span></th>
<th><span data-ttu-id="831d9-124">&lt;Einstellung "dpiAwareness" &gt; (Windows 10, Version 1607 und höher)</span><span class="sxs-lookup"><span data-stu-id="831d9-124">&lt;dpiAwareness&gt; setting (Windows 10, version 1607 and later)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="831d9-125">nicht bekannt</span><span class="sxs-lookup"><span data-stu-id="831d9-125">unaware</span></span></td>
<td><p><span data-ttu-id="831d9-126">N/A (keine DpiAware-Einstellung im Manifest)</span><span class="sxs-lookup"><span data-stu-id="831d9-126">N/A (no dpiAware setting in manifest)</span></span></p>
<p><span data-ttu-id="831d9-127">oder</span><span class="sxs-lookup"><span data-stu-id="831d9-127">or</span></span></p>
<p><span data-ttu-id="831d9-128">&lt;dpiAware &gt; false &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="831d9-128">&lt;dpiAware&gt;false&lt;/dpiAware&gt;</span></span></p></td>
<td><span data-ttu-id="831d9-129">&lt;DpiAwareness &gt; nicht bekannt &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="831d9-129">&lt;dpiAwareness&gt;unaware&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="831d9-130">Systembewusst</span><span class="sxs-lookup"><span data-stu-id="831d9-130">System aware</span></span></td>
<td><span data-ttu-id="831d9-131">&lt;dpiAware &gt; true &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="831d9-131">&lt;dpiAware&gt;true&lt;/dpiAware&gt;</span></span></td>
<td><span data-ttu-id="831d9-132">&lt;dpiAwareness &gt; system &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="831d9-132">&lt;dpiAwareness&gt;system&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="831d9-133">Pro Monitor</span><span class="sxs-lookup"><span data-stu-id="831d9-133">Per Monitor</span></span></td>
<td><span data-ttu-id="831d9-134">&lt;dpiAware &gt; true/pm &lt; dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="831d9-134">&lt;dpiAware&gt;true/pm&lt;dpiAware&gt;</span></span></td>
<td><span data-ttu-id="831d9-135">&lt;dpiAwareness &gt; PerMonitor &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="831d9-135">&lt;dpiAwareness&gt;PerMonitor&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="831d9-136">Pro Monitor V2</span><span class="sxs-lookup"><span data-stu-id="831d9-136">Per Monitor V2</span></span></td>
<td><span data-ttu-id="831d9-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="831d9-137">Not supported</span></span></td>
<td><span data-ttu-id="831d9-138">&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="831d9-138">&lt;dpiAwareness&gt;PerMonitorV2&lt;/dpiAwareness&gt;</span></span></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="831d9-139">Das folgende Beispiel zeigt sowohl die - als auch die -Einstellungen, die in derselben Manifestdatei verwendet werden, um das \<dpiAwareness\> Prozess-Standard-DPI-Bewusstseinsverhalten für verschiedene Versionen von \<dpiAware\> Windows.</span><span class="sxs-lookup"><span data-stu-id="831d9-139">The sample below shows both the \<dpiAwareness\> and the \<dpiAware\> settings being used within the same manifest file to configure process-default DPI awareness behavior for different versions of Windows.</span></span>

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

## <a name="setting-default-awareness-programmatically"></a><span data-ttu-id="831d9-140">Programmgesteuertes Festlegen des Standardbewusstseins</span><span class="sxs-lookup"><span data-stu-id="831d9-140">Setting default awareness programmatically</span></span>

<span data-ttu-id="831d9-141">Obwohl dies nicht empfohlen wird, ist es möglich, die Standardmäßige DPI-Kenntnis programmgesteuert festlegen.</span><span class="sxs-lookup"><span data-stu-id="831d9-141">Although it is not recommended, it is possible to set the default DPI awareness programmatically.</span></span> <span data-ttu-id="831d9-142">Sobald ein Fenster (ein HWND) in Ihrem Prozess erstellt wurde, wird das Ändern des DPI-Bewusstseinsmodus nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="831d9-142">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="831d9-143">Wenn Sie den standardmäßigen Prozess-DPI-Bewusstseinsmodus programmgesteuert festlegen, müssen Sie die entsprechende API aufrufen, bevor HWNDs erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="831d9-143">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span>

<span data-ttu-id="831d9-144">Es gibt mehrere APIs, mit denen Sie die DPI-Standarderlädung für Ihren Prozess angeben können.</span><span class="sxs-lookup"><span data-stu-id="831d9-144">There are multiple APIs that let you specify the default DPI awareness for your process.</span></span> <span data-ttu-id="831d9-145">Die derzeit empfohlene API ist [**SetProcessDpiAwarenessContext,**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))da ältere APIs weniger Funktionalität bieten.</span><span class="sxs-lookup"><span data-stu-id="831d9-145">The current recommended API is [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), as older APIs offer less functionality.</span></span>

 

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
<th><span data-ttu-id="831d9-146">API</span><span class="sxs-lookup"><span data-stu-id="831d9-146">API</span></span></th>
<th><span data-ttu-id="831d9-147">Mindestversion der Windows</span><span class="sxs-lookup"><span data-stu-id="831d9-147">Minimum version of Windows</span></span></th>
<th><span data-ttu-id="831d9-148">DPI nicht bekannt</span><span class="sxs-lookup"><span data-stu-id="831d9-148">DPI Unaware</span></span></th>
<th><span data-ttu-id="831d9-149">System-DPI-bewusst</span><span class="sxs-lookup"><span data-stu-id="831d9-149">System DPI Aware</span></span></th>
<th><span data-ttu-id="831d9-150">DPI-bewusst pro Monitor</span><span class="sxs-lookup"><span data-stu-id="831d9-150">Per Monitor DPI Aware</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="831d9-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></span><span class="sxs-lookup"><span data-stu-id="831d9-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></span></span></td>
<td><span data-ttu-id="831d9-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="831d9-152">Windows Vista</span></span></td>
<td><span data-ttu-id="831d9-153">–</span><span class="sxs-lookup"><span data-stu-id="831d9-153">N/A</span></span></td>
<td><span data-ttu-id="831d9-154">SetProcessDPIAware()</span><span class="sxs-lookup"><span data-stu-id="831d9-154">SetProcessDPIAware()</span></span></td>
<td><span data-ttu-id="831d9-155">–</span><span class="sxs-lookup"><span data-stu-id="831d9-155">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="831d9-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span><span class="sxs-lookup"><span data-stu-id="831d9-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span></span></td>
<td><span data-ttu-id="831d9-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="831d9-157">Windows 8.1</span></span></td>
<td><span data-ttu-id="831d9-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="831d9-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span></span></td>
<td><span data-ttu-id="831d9-159">SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="831d9-159">SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE)</span></span></td>
<td><span data-ttu-id="831d9-160">SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="831d9-160">SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="831d9-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="831d9-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span></span></td>
<td><span data-ttu-id="831d9-162">Windows 10, Version 1607</span><span class="sxs-lookup"><span data-stu-id="831d9-162">Windows 10, version 1607</span></span></td>
<td><span data-ttu-id="831d9-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="831d9-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span></span></td>
<td><span data-ttu-id="831d9-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span><span class="sxs-lookup"><span data-stu-id="831d9-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span></span></td>
<td><p><span data-ttu-id="831d9-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span><span class="sxs-lookup"><span data-stu-id="831d9-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span></span></p>
<p><span data-ttu-id="831d9-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span><span class="sxs-lookup"><span data-stu-id="831d9-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a><span data-ttu-id="831d9-167">Prozess-Standard und Thread-Standard</span><span class="sxs-lookup"><span data-stu-id="831d9-167">Process-default vs. Thread default</span></span>

<span data-ttu-id="831d9-168">Dieses Dokument bezieht sich auf das Festlegen des DPI-Standardbewusstseins für Ihren Prozess.</span><span class="sxs-lookup"><span data-stu-id="831d9-168">This document refers to setting the default DPI awareness for your process.</span></span> <span data-ttu-id="831d9-169">Dies liegt daran, Windows 10 unterstützung für die Ausführung von mehr als einem DPI-Bewusstseinsmodus innerhalb eines einzelnen Prozesses eingeführt hat (vor Windows 10 musste der gesamte Prozess einem einzelnen DPI-Bewusstseinsmodus entsprechen).</span><span class="sxs-lookup"><span data-stu-id="831d9-169">This is because Windows 10 introduced support for running more than one DPI awareness mode within a single process (prior to Windows 10, the entire process had to conform to a single DPI awareness mode).</span></span> <span data-ttu-id="831d9-170">Die Unterstützung für die Ausführung von mehr als einem DPI-Bewusstseinsmodus innerhalb eines Prozesses wird als "DPI-Skalierung im gemischten Modus" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="831d9-170">Support for running more than one DPI awareness mode within a process is referred to as "mixed-mode DPI scaling".</span></span> <span data-ttu-id="831d9-171">Wenn Sie die DPI-Skalierung im gemischten Modus in Ihrem Prozess verwenden, kann jedes Fenster der obersten Ebene in einem DPI-Bewusstseinsmodus ausgeführt werden, der sich möglicherweise von dem des Standardprozesses unterscheiden kann.</span><span class="sxs-lookup"><span data-stu-id="831d9-171">When using mixed-mode DPI scaling within your process, each top-level Window can run in a DPI awareness mode that may be different than that of the process default.</span></span> <span data-ttu-id="831d9-172">Sofern nicht explizit angegeben, wird für jeden Thread standardmäßig der Standardprozess verwendet, wenn er erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="831d9-172">Unless explicitly specified, each thread will default to the process default when created.</span></span> <span data-ttu-id="831d9-173">Weitere Informationen zur DPI-Skalierung im gemischten Modus finden Sie im Artikel [DPI-Skalierung im gemischten](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) Modus.</span><span class="sxs-lookup"><span data-stu-id="831d9-173">For more information about mixed-mode DPI scaling, refer to the [Mixed-Mode DPI Scaling](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) article.</span></span>
