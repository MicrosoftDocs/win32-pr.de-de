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
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Festlegen des DPI-Standardbewusstseins für einen Prozess

Desktopanwendungen auf Windows können in verschiedenen DPI-Bewusstseinsmodi ausgeführt werden. Diese Modi ermöglichen ein anderes DPI-Skalierungsverhalten und können unterschiedliche Koordinatenräume verwenden. Weitere Informationen zur DPI-Bekanntheit finden Sie unter [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) Es ist wichtig, dass Sie explizit den standardmäßigen DPI-Bewusstseinsmodus Ihres Prozesses festlegen, um unerwartetes Verhalten zu vermeiden.

Es gibt zwei Hauptmethoden, um die Standard-DPI-Kenntnis eines Prozesses anzugeben:

1 \) bis zu einer Anwendungsmanifesteinstellung

2 \) programmgesteuert über einen API-Aufruf

Es wird empfohlen, den DPI-Standardprozess über eine Manifesteinstellung anzugeben. Die Angabe des Standardwerts über die API wird zwar unterstützt, wird jedoch nicht empfohlen.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Festlegen des Standardbewusstseins mit dem Anwendungsmanifest

Es gibt zwei Manifesteinstellungen, mit denen Sie den Standardmäßigen DPI-Aktivierungsmodus des Prozesses angeben können: \<dpiAwareness\> und \<dpiAware\> . \<dpiAware\>wurde in Windows Vista eingeführt und ermöglicht nur, dass Ihr Prozess standardmäßig auf Systembewusstsein festgelegt wird. \<dpiAwareness\>wurde in Windows 10 Version 1607 eingeführt und ermöglicht ihnen das Angeben einer geordneten Liste von prozessbasierten DPI-Awareness-Modi. Dadurch können Sie Sicherungs-DPI-Awareness-Modi festlegen, die verwendet werden, wenn Ihre Anwendung auf einer Version von ausgeführt wird, Windows den ersten angegebenen Bewusstseinsmodus nicht unterstützen kann. Bei älteren Windows wird das neuere Tag \<dpiAwareness\> ignoriert. Dies bedeutet, dass Sie beide Manifesteinstellungen verwenden können, um ein Szenario zu ermöglichen, in dem Ihre Prozesseinstellung auf ältere Versionen von Windows festgelegt werden kann, während sie Per-Monitor für Versionen größer als Windows 10, Version 1607, verwendet werden. In Windows 10 Version 1607 und on wird die Einstellung \<dpiAware\> ignoriert, wenn \<dpiAwareness\> das Element vorhanden ist.

In der folgenden Tabelle wird gezeigt, wie sie mithilfe der beiden Manifesteinstellungen unterschiedliche Prozess-Standard-DPI-Bewusstseinsmodi angeben:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Verarbeiten des standardmäßigen DPI-Bewusstseinsmodus</th>
<th>&lt;dpiAware-Einstellung &gt;</th>
<th>&lt;Einstellung "dpiAwareness" &gt; (Windows 10, Version 1607 und höher)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>nicht bekannt</td>
<td><p>N/A (keine DpiAware-Einstellung im Manifest)</p>
<p>oder</p>
<p>&lt;dpiAware &gt; false &lt; /dpiAware&gt;</p></td>
<td>&lt;DpiAwareness &gt; nicht bekannt &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>Systembewusst</td>
<td>&lt;dpiAware &gt; true &lt; /dpiAware&gt;</td>
<td>&lt;dpiAwareness &gt; system &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="odd">
<td>Pro Monitor</td>
<td>&lt;dpiAware &gt; true/pm &lt; dpiAware&gt;</td>
<td>&lt;dpiAwareness &gt; PerMonitor &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>Pro Monitor V2</td>
<td>Nicht unterstützt</td>
<td>&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</td>
</tr>
</tbody>
</table>

 

Das folgende Beispiel zeigt sowohl die - als auch die -Einstellungen, die in derselben Manifestdatei verwendet werden, um das \<dpiAwareness\> Prozess-Standard-DPI-Bewusstseinsverhalten für verschiedene Versionen von \<dpiAware\> Windows.

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

## <a name="setting-default-awareness-programmatically"></a>Programmgesteuertes Festlegen des Standardbewusstseins

Obwohl dies nicht empfohlen wird, ist es möglich, die Standardmäßige DPI-Kenntnis programmgesteuert festlegen. Sobald ein Fenster (ein HWND) in Ihrem Prozess erstellt wurde, wird das Ändern des DPI-Bewusstseinsmodus nicht mehr unterstützt. Wenn Sie den standardmäßigen Prozess-DPI-Bewusstseinsmodus programmgesteuert festlegen, müssen Sie die entsprechende API aufrufen, bevor HWNDs erstellt wurden.

Es gibt mehrere APIs, mit denen Sie die DPI-Standarderlädung für Ihren Prozess angeben können. Die derzeit empfohlene API ist [**SetProcessDpiAwarenessContext,**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))da ältere APIs weniger Funktionalität bieten.

 

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
<th>API</th>
<th>Mindestversion der Windows</th>
<th>DPI nicht bekannt</th>
<th>System-DPI-bewusst</th>
<th>DPI-bewusst pro Monitor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></td>
<td>Windows Vista</td>
<td>–</td>
<td>SetProcessDPIAware()</td>
<td>–</td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></td>
<td>Windows 8.1</td>
<td>SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</td>
<td>SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE)</td>
<td>SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE)</td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></td>
<td>Windows 10, Version 1607</td>
<td>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</td>
<td>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</td>
<td><p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p>
<p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a>Prozess-Standard und Thread-Standard

Dieses Dokument bezieht sich auf das Festlegen des DPI-Standardbewusstseins für Ihren Prozess. Dies liegt daran, Windows 10 unterstützung für die Ausführung von mehr als einem DPI-Bewusstseinsmodus innerhalb eines einzelnen Prozesses eingeführt hat (vor Windows 10 musste der gesamte Prozess einem einzelnen DPI-Bewusstseinsmodus entsprechen). Die Unterstützung für die Ausführung von mehr als einem DPI-Bewusstseinsmodus innerhalb eines Prozesses wird als "DPI-Skalierung im gemischten Modus" bezeichnet. Wenn Sie die DPI-Skalierung im gemischten Modus in Ihrem Prozess verwenden, kann jedes Fenster der obersten Ebene in einem DPI-Bewusstseinsmodus ausgeführt werden, der sich möglicherweise von dem des Standardprozesses unterscheiden kann. Sofern nicht explizit angegeben, wird für jeden Thread standardmäßig der Standardprozess verwendet, wenn er erstellt wird. Weitere Informationen zur DPI-Skalierung im gemischten Modus finden Sie im Artikel [DPI-Skalierung im gemischten](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) Modus.
