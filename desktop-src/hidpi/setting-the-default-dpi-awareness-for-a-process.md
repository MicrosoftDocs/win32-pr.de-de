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
ms.openlocfilehash: 216952ac05811226c403739d389f8de9f636c3b8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880526"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Festlegen des DPI-Standardbewusstseins für einen Prozess

Desktopanwendungen auf Windows können in verschiedenen DPI-Bewusstseinsmodi ausgeführt werden. Diese Modi ermöglichen ein anderes DPI-Skalierungsverhalten und können unterschiedliche Koordinatenräume verwenden. Weitere Informationen zur DPI-Kenntnis finden Sie unter [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) Es ist wichtig, dass Sie explizit den standardmäßigen DPI-Bewusstseinsmodus Ihres Prozesses festlegen, um unerwartetes Verhalten zu vermeiden.

Es gibt zwei Hauptmethoden, um die Standard-DPI-Kenntnis eines Prozesses anzugeben:

1 \) bis zu einer Anwendungsmanifesteinstellung

2 \) programmgesteuert über einen API-Aufruf

Es wird empfohlen, den DPI-Standardprozess über eine Manifesteinstellung anzugeben. Die Angabe des Standardwerts über die API wird zwar unterstützt, wird jedoch nicht empfohlen.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Festlegen des Standardbewusstseins mit dem Anwendungsmanifest

Es gibt zwei Manifesteinstellungen, mit denen Sie den Standardmäßigen DPI-Aktivierungsmodus des Prozesses angeben können: \<dpiAwareness\> und \<dpiAware\> . \<dpiAware\>wurde in Windows Vista eingeführt und ermöglicht nur, dass Ihr Prozess standardmäßig auf Systembewusstsein festgelegt wird. \<dpiAwareness\>wurde in Windows 10 Version 1607 eingeführt und ermöglicht ihnen das Angeben einer geordneten Liste von Prozess-Standard-DPI-Bewusstseinsmodi. Dadurch können Sie Sicherungs-DPI-Awareness-Modi festlegen, die verwendet werden, wenn Ihre Anwendung auf einer Version von ausgeführt wird, Windows den ersten angegebenen Bewusstseinsmodus nicht unterstützen kann. Bei älteren Windows wird das neuere Tag \<dpiAwareness\> ignoriert. Dies bedeutet, dass Sie beide Manifesteinstellungen verwenden können, um ein Szenario zu ermöglichen, in dem Ihre Prozesseinstellung auf ältere Versionen von Windows festgelegt werden kann, während sie Per-Monitor versionen größer als Windows 10 Version 1607 sind. Bei Windows 10 Version 1607 und on wird die Einstellung \<dpiAware\> ignoriert, wenn \<dpiAwareness\> das Element vorhanden ist.

In der folgenden Tabelle wird gezeigt, wie Sie mithilfe der beiden Manifesteinstellungen unterschiedliche DPI-Standard-Prozess-DPI-Bewusstseinsmodi angeben:


| Verarbeiten des standardmäßigen DPI-Bewusstseinsmodus | &lt;dpiAware-Einstellung &gt; | &lt;Einstellung "dpiAwareness" &gt; (Windows 10, Version 1607 und höher) | 
|------------------------------------|--------------------|--------------------------------------------------------------|
| nicht bekannt | <p>N/A (keine DpiAware-Einstellung im Manifest)</p><p>oder</p><p>&lt;dpiAware &gt; false &lt; /dpiAware&gt;</p> | &lt;DpiAwareness &gt; nicht bekannt &lt; /dpiAwareness&gt; | 
| Systembewusst | &lt;dpiAware &gt; true &lt; /dpiAware&gt; | &lt;dpiAwareness &gt; system &lt; /dpiAwareness&gt; | 
| Pro Monitor | &lt;dpiAware &gt; true/pm &lt; dpiAware&gt; | &lt;dpiAwareness &gt; PerMonitor &lt; /dpiAwareness&gt; | 
| Pro Monitor V2 | Nicht unterstützt | &lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt; | 


 

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

 


| API | Mindestversion Windows | DPI nicht bekannt | System-DPI-bewusst | DPI-bewusst pro Monitor | 
|-----|----------------------------|-------------|------------------|-----------------------|
| <a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a> | Windows Vista | – | SetProcessDPIAware() | – | 
| <a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a> | Windows 8.1 | SetProcessDpiAwareness(PROCESS_DPI_UNAWARE) | SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE) | SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE) | 
| <a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a> | Windows 10, Version 1607 | SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE) | SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE) | <p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p><p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p> | 


 

## <a name="process-default-vs-thread-default"></a>Prozess-Standard im Vergleich zu Thread-Standard

Dieses Dokument bezieht sich auf das Festlegen des DPI-Standardbewusstseins für Ihren Prozess. Dies liegt daran, Windows 10 unterstützung für die Ausführung von mehr als einem DPI-Bewusstseinsmodus innerhalb eines einzelnen Prozesses eingeführt hat (vor Windows 10 musste der gesamte Prozess einem einzelnen DPI-Bewusstseinsmodus entsprechen). Die Unterstützung für die Ausführung von mehr als einem DPI-Bewusstseinsmodus innerhalb eines Prozesses wird als "DPI-Skalierung im gemischten Modus" bezeichnet. Wenn Sie die DPI-Skalierung im gemischten Modus in Ihrem Prozess verwenden, kann jedes Fenster der obersten Ebene in einem DPI-Bewusstseinsmodus ausgeführt werden, der sich möglicherweise von dem des Standardprozesses unterscheiden kann. Sofern nicht explizit angegeben, wird für jeden Thread standardmäßig der Standardprozess verwendet, wenn er erstellt wird. Weitere Informationen zur DPI-Skalierung im gemischten Modus finden Sie im Artikel [DPI-Skalierung im gemischten](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) Modus.
