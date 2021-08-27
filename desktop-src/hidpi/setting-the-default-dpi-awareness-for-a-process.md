---
description: Weitere Informationen finden Sie unter Festlegen der DPI-Standarderkennung für einen Prozess.
title: Festlegen der DPI-Standarderkennung für einen Prozess (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: 52ef4f10ed2f4253c796ae10a57a71d8a7bc4f0d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465677"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Festlegen der DPI-Standarderkennung für einen Prozess

Desktopanwendungen auf Windows können in verschiedenen DPI-Erkennungsmodi ausgeführt werden. Diese Modi ermöglichen ein anderes DPI-Skalierungsverhalten und können unterschiedliche Koordinatenräume verwenden. Weitere Informationen zur DPI-Erkennung finden Sie unter [High DPI Desktop Application Development on Windows (Entwicklung von Desktopanwendungen mit hohem DPI-Anteil auf Windows).](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) Es ist wichtig, dass Sie explizit den DPI-Standarderkennungsmodus Ihres Prozesses festlegen, um unerwartetes Verhalten zu vermeiden.

Es gibt zwei Hauptmethoden, um die DPI-Standarderkennung eines Prozesses anzugeben:

1 \) über eine Anwendungsmanifesteinstellung

2 \) programmgesteuert über einen API-Aufruf

Es wird empfohlen, die Standardmäßige Prozess-DPI-Kenntnis über eine Manifesteinstellung anzugeben. Die Angabe des Standardwerts über die API wird zwar unterstützt, wird jedoch nicht empfohlen.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Festlegen der Standarderkennung mit dem Anwendungsmanifest

Es gibt zwei Manifesteinstellungen, mit denen Sie den Standardmäßigen DPI-Prozesserkennungsmodus angeben können: \<dpiAwareness\> und \<dpiAware\> . \<dpiAware\>wurde in Windows Vista eingeführt und ermöglicht nur, dass der Prozessstandard auf Systemerkennung festgelegt wird. \<dpiAwareness\>wurde in Windows 10 Version 1607 eingeführt und ermöglicht es Ihnen, eine geordnete Liste der prozessstandardbasierten DPI-Erkennungsmodi anzugeben. Auf diese Weise können Sie Sicherungs-DPI-Erkennungsmodi festlegen, die verwendet werden, wenn Ihre Anwendung auf einer Version von ausgeführt wird Windows den ersten angegebenen Awareness-Modus nicht unterstützen können. Bei älteren Versionen von Windows wird das \<dpiAwareness\> neuere Tag ignoriert. Dies bedeutet, dass Sie beide Manifesteinstellungen verwenden können, um ein Szenario zu ermöglichen, in dem Der Prozessstandard für ältere Versionen von Windows systemfähig sein kann, während er in Versionen größer als Windows 10 Version 1607 Per-Monitor wird. Auf Windows 10 Version 1607 und höher wird die \<dpiAware\> Einstellung ignoriert, wenn das \<dpiAwareness\> Element vorhanden ist.

In der folgenden Tabelle wird gezeigt, wie sie verschiedene Prozessstandard-DPI-Awareness-Modi mithilfe der beiden Manifesteinstellungen angeben:


| Verarbeiten des DPI-Standarderkennungsmodus | <dpiAware>-Einstellung | <dpiAwareness>-Einstellung (Windows 10, Version 1607 und höher) | 
|------------------------------------|--------------------|--------------------------------------------------------------|
| nicht bekannt | <p>N/A (keine dpiAware-Einstellung im Manifest)</p><p>oder</p><p>&lt;dpiAware &gt; false &lt; /dpiAware&gt;</p> | <dpiAwareness>nicht bekannt</dpiAwareness> | 
| Systemfähiges System | <dpiAware>true</dpiAware> | <dpiAwareness>System</dpiAwareness> | 
| Pro Monitor | <dpiAware>true/pm<dpiAware> | <dpiAwareness>PerMonitor</dpiAwareness> | 
| Pro Monitor V2 | Nicht unterstützt | <dpiAwareness>PerMonitorV2</dpiAwareness> | 


 

Das folgende Beispiel zeigt sowohl die Einstellungen als auch \<dpiAwareness\> die Einstellungen, die \<dpiAware\> in derselben Manifestdatei verwendet werden, um das prozessstandardbasierte DPI-Bewusstseinsverhalten für verschiedene Versionen von Windows zu konfigurieren.

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

## <a name="setting-default-awareness-programmatically"></a>Programmgesteuertes Festlegen der Standarderkennung

Obwohl dies nicht empfohlen wird, ist es möglich, die DPI-Standarderkennung programmgesteuert festzulegen. Sobald ein Fenster (ein HWND) in Ihrem Prozess erstellt wurde, wird das Ändern des DPI-Erkennungsmodus nicht mehr unterstützt. Wenn Sie den Prozessstandard-DPI-Modus programmgesteuert festlegen, müssen Sie die entsprechende API aufrufen, bevor HWNDs erstellt wurden.

Es gibt mehrere APIs, mit denen Sie die DPI-Standarderkennung für Ihren Prozess angeben können. Die derzeit empfohlene API ist [**SetProcessDpiAwarenessContext,**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))da ältere APIs weniger Funktionalität bieten.

 


| API | Mindestversion von Windows | DPI nicht bekannt | System-DPI-fähigen | DPI-fähige Daten pro Monitor | 
|-----|----------------------------|-------------|------------------|-----------------------|
| <a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a> | Windows Vista | – | SetProcessDPIAware() | – | 
| <a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a> | Windows 8.1 | SetProcessDpiAwareness(PROCESS_DPI_UNAWARE) | SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE) | SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE) | 
| <a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a> | Windows 10, Version 1607 | SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE) | SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE) | <p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p><p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p> | 


 

## <a name="process-default-vs-thread-default"></a>Prozessstandard im Vergleich zu Threadstandard

Dieses Dokument bezieht sich auf das Festlegen der DPI-Standarderkennung für Ihren Prozess. Dies liegt daran, dass Windows 10 unterstützung für die Ausführung mehrerer DPI-Awareness-Modi innerhalb eines einzelnen Prozesses eingeführt haben (vor Windows 10 musste der gesamte Prozess einem einzelnen DPI-Awareness-Modus entsprechen). Unterstützung für die Ausführung mehrerer DPI-Awareness-Modus innerhalb eines Prozesses wird als "DPI-Skalierung im gemischten Modus" bezeichnet. Wenn Sie die DPI-Skalierung im gemischten Modus innerhalb Ihres Prozesses verwenden, kann jedes Fenster der obersten Ebene in einem DPI-Modus ausgeführt werden, der sich von dem des Prozessstandardmodus unterscheidet. Sofern nicht explizit angegeben, wird bei der Erstellung für jeden Thread standardmäßig der Prozessstandard verwendet. Weitere Informationen zur DPI-Skalierung im gemischten Modus finden Sie im Artikel [DPI-Skalierung im gemischten Modus.](https://msdn.microsoft.com/library/mt744321\(v=vs.85\))
