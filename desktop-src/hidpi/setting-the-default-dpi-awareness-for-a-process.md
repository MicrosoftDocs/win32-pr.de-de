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
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Festlegen der Standard-dpi-Informationen für einen Prozess

Desktop Anwendungen unter Windows können in unterschiedlichen dpi-Methoden ausgeführt werden. Diese Modi ermöglichen verschiedene dpi-Skalierungs Verhalten und können unterschiedliche Koordinaten Bereiche verwenden. Weitere Informationen zu dpi-Informationen finden Sie unter [hohe dpi-Entwicklung für Desktop Anwendungen unter Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) Es ist wichtig, dass Sie den standardmäßigen dpi-Informationsmodus des Prozesses explizit festlegen, um unerwartetes Verhalten zu vermeiden.

Es gibt zwei Hauptmethoden, um das standardmäßige dpi-Bewusstsein eines Prozesses anzugeben:

1 \) durch eine Einstellung für das Anwendungs Manifest

2 Programm gesteuertes ausführen \) eines API-Aufrufes

Es wird empfohlen, dass Sie den Standardprozess-dpi-Wert über eine Manifest-Einstellung angeben. Die Angabe der standardmäßigen via-API wird zwar unterstützt, es wird jedoch nicht empfohlen.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Festlegen von Standard Bekanntheit mit dem Anwendungs Manifest

Es gibt zwei Manifest-Einstellungen, mit denen Sie den Prozessstandard-dpi-Awareness-Modus angeben können: \<dpiAwareness\> und \<dpiAware\> . \<dpiAware\> wurde in Windows Vista eingeführt und ermöglicht nur, dass Ihr ProzessStandard mäßig auf System Bewusstsein festgelegt ist. \<dpiAwareness\> wurde in Windows 10, Version 1607, eingeführt und ermöglicht Ihnen das Angeben einer geordneten Liste von Prozess-Standard-dpi-Informations Modi. Dies ermöglicht es Ihnen, die Kompatibilitäts Modi für die Sicherung festzulegen, die verwendet werden, wenn Ihre Anwendung auf einer Version von Windows ausgeführt wird und den ersten angegebenen Informationsmodus nicht unterstützen kann. In älteren Versionen von Windows wird das neuere \<dpiAwareness\> Tag ignoriert. Dies bedeutet, dass Sie beide Manifest-Einstellungen verwenden können, um ein Szenario zu aktivieren, bei dem der ProzessStandard bei der Per-Monitor unter Windows 10, Version 1607, Systeminformationen für ältere Windows-Versionen ist. Unter Windows 10, Version 1607 und auf, wird die \<dpiAware\> Einstellung ignoriert, wenn das \<dpiAwareness\> Element vorhanden ist.

In der folgenden Tabelle wird gezeigt, wie verschiedene ProzessStandard-dpi-Informations Modi mithilfe der beiden Manifest-Einstellungen angegeben werden:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Standard-dpi-Modus verarbeiten</th>
<th>&lt;dpiaware- &gt; Einstellung</th>
<th>&lt;dpiawareness &gt; -Einstellung (Windows 10, Version 1607 und höher)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>bewusste</td>
<td><p>N/v (keine dpiaware-Einstellung im Manifest)</p>
<p>oder</p>
<p>&lt;dpiaware &gt; false &lt; /dpiAware&gt;</p></td>
<td>&lt;dpiawareness ist &gt; nicht bekannt &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>System fähig</td>
<td>&lt;dpiaware &gt; true &lt; /dpiAware&gt;</td>
<td>&lt;dpiawareness- &gt; System &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="odd">
<td>Pro Monitor</td>
<td>&lt;dpiaware &gt; true/PM &lt; dpiaware&gt;</td>
<td>&lt;dpiawareness &gt; permonitor &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>Pro Monitor v2</td>
<td>Nicht unterstützt</td>
<td>&lt;dpiawareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</td>
</tr>
</tbody>
</table>

 

Das folgende Beispiel zeigt sowohl die \<dpiAwareness\> -als auch die-Einstellungen, die \<dpiAware\> in derselben Manifest-Datei verwendet werden, um das Prozess-Standardverhalten des dpi-Manifests für verschiedene Versionen von Windows zu konfigurieren.

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

## <a name="setting-default-awareness-programmatically"></a>Programm gesteuertes Festlegen von Standardinformationen

Obwohl es nicht empfohlen wird, ist es möglich, das standardmäßige dpi-Bewusstsein Programm gesteuert festzulegen. Sobald ein Fenster (ein HWND) in Ihrem Prozess erstellt wurde, wird das Ändern des dpi-Informationsmodus nicht mehr unterstützt. Wenn Sie den Prozess-Standard-dpi-Informationsmodus Programm gesteuert festlegen, müssen Sie die entsprechende API vor dem Erstellen von HWNDs aufruft.

Es gibt mehrere APIs, mit denen Sie das standardmäßige dpi-Bewusstsein für Ihren Prozess angeben können. Die aktuelle empfohlene API ist " [**setprocessdpiawarsess Context**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))", da ältere APIs weniger Funktionen bieten.

 

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
<th>Mindestversion von Windows</th>
<th>DPI nicht bekannt</th>
<th>System-dpi-fähig</th>
<th>DPI-Erkennung pro Monitor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></td>
<td>Windows Vista</td>
<td>–</td>
<td>SetProcessDPIAware ()</td>
<td>–</td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>Setprocessdpiawareness</strong></a></td>
<td>Windows 8.1</td>
<td>Setprocessdpiawareness (PROCESS_DPI_UNAWARE)</td>
<td>Setprocessdpiawareness (PROCESS_DPI_SYSTEM_DPI_AWARE)</td>
<td>Setprocessdpiawareness (PROCESS_DPI_PER_MONITOR_DPI_AWARE)</td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>Setprocessdpiawareress Context</strong></a></td>
<td>Windows 10, Version 1607</td>
<td>Setprocessdpiawareress Context (DPI_AWARENESS_CONTEXT_UNAWARE)</td>
<td>Setprocessdpiawareress Context (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</td>
<td><p>Setprocessdpiawareress Context (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p>
<p>Setprocessdpiawareress Context (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a>Prozess-Standard Vergleich und Thread Standard

Dieses Dokument bezieht sich auf das Festlegen der Standard-dpi-Informationen für den Prozess. Dies liegt daran, dass Windows 10 die Unterstützung für die Ausführung von mehr als einem dpi-Modus in einem einzelnen Prozess (vor Windows 10) eingeführt hat (vor Windows 10 musste der gesamte Prozess einem einzigen dpi-Awareness-Modus entsprechen). Die Unterstützung für das Ausführen von mehr als einem dpi-Informationsmodus innerhalb eines Prozesses wird als "DPI-Skalierung im gemischten Modus" bezeichnet. Wenn Sie die DPI-Skalierung im gemischten Modus innerhalb des Prozesses verwenden, kann jedes Fenster der obersten Ebene in einem dpi-Modus ausgeführt werden, der sich von der Standardeinstellung des Prozesses unterscheiden kann. Sofern nicht explizit angegeben, wird jeder Thread bei der Erstellung standardmäßig auf den Standardprozess eingestellt. Weitere Informationen zur DPI-Skalierung im gemischten Modus finden Sie im Artikel zur [DPI-Skalierung im gemischten Modus](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .
