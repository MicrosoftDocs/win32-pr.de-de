---
title: Kompatibilität und Zuverlässigkeit
description: Windows 7 ist so konzipiert, dass es auf derselben Hardware wie Windows Vista ausgeführt wird und mit Anwendungen und Gerätetreibern kompatibel ist, die mit Windows Vista funktionieren.
ms.assetid: d7a0c335-93d1-49d3-ae40-c59ff9163f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e9686c732c94b4b99408d0fd6e24f84079ee9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340730"
---
# <a name="compatibility-and-reliability"></a>Kompatibilität und Zuverlässigkeit

Windows 7 ist so konzipiert, dass es auf derselben Hardware wie Windows Vista ausgeführt wird und mit Anwendungen und Gerätetreibern kompatibel ist, die mit Windows Vista funktionieren.

Windows 7 ist die zuverlässigste Version von Windows. Windows 7 wurde auf einer verbesserten Technologie Foundation entwickelt und ermöglicht es Benutzern, ihre Computer zuverlässig zu starten, herunterzufahren oder in den Ruhezustand zu versetzen, ohne sich Gedanken über den Verlust von wertvollen Arbeit machen zu müssen. Darüber hinaus vereinfacht Windows 7 das Sichern und Wiederherstellen von Daten auf Netzlaufwerken oder Digital Video Disks (DVDs). Windows 7 verbessert auch die Druck Zuverlässigkeit und-Leistung. (Weitere Informationen finden [Sie unter Windows 7 Application Quality Cookbook](../win7appqual/windows-7-application-quality-cookbook.md).)

## <a name="applications"></a>Anwendungen

Um die Kompatibilität zu gewährleisten, wurde Windows 7 in enger Partnerschaft mit Softwareherstellern und PC-Herstellern entwickelt. Frühe Einbindung hat Microsoft ermöglicht, eine umfassende Liste der am häufigsten verwendeten Anwendungen zu erstellen. Automatisierte Testzyklen stellen sicher, dass Kompatibilitätsprobleme früh im Entwicklungszyklus erkannt und behoben werden. (Siehe [Windows-Anwendungs Kompatibilität](/windows/apps/desktop/).)

## <a name="drivers"></a>Treiber

Die Version des Windows Driver Kit (WDK) 7.0.0 bietet die Buildumgebung, Tools, Dokumentation und Beispiele, die Entwickler zum Erstellen von Qualitäts Treibern für Windows benötigen. Das WDK 7.0.0 unterstützt die statische Quell Code Analyse mithilfe von PREfast, um bestimmte Klassen von C-und C++-Codierungs Fehlern zu erkennen. PREfast enthält eine spezialisierte Treiber Komponente, die als "PREfast for Drivers" (PFD) bezeichnet wird, die Fehler im Kernelmodustreiber-Code erkennt. Außerdem wurde das WDK durch kommentieren aller Kernel Header Dateien für die PFD-Unterstützung verbessert. Es wurden neue Beispiel Treiber hinzugefügt, die neue Technologien veranschaulichen, und die Dokumentation wurde erweitert.

Windows 7 unterstützt eine Vielzahl von Software-und Hardwareprodukten, die für eine nahtlose Integration in die Plattform konzipiert sind. Treiber, die für Windows Vista erstellt wurden, sollten für die ordnungsgemäße Verwendung in Windows 7 nicht aktualisiert werden. (Siehe [Windows-Treiberkit](/windows-hardware/drivers/).)

## <a name="devices"></a>Geräte

Windows 7 bietet eine flexible, robuste Unterstützung für eine Vielzahl von Anwendungen und Geräten, darunter Musikplayer, Speichergeräte, Mobiltelefone und andere Arten von verbundenen Geräten. Das automatische Testen dieser Geräte wird verwendet, um sicherzustellen, dass Kompatibilitätsprobleme früh im Entwicklungszeitraum behoben werden. (Siehe [Grundlagen der Windows-Geräteklasse](https://www.microsoft.com/whdc/device/default.mspx).)

## <a name="reliability-analysis-component"></a>Zuverlässigkeitsanalyse Komponente

Die Zuverlässigkeitsanalysekomponente ist ein Posteingangsagent, der ausführliche Kundenfeedbackinfos zur Systemauslastung und -zuverlässigkeit bereitstellt. Diese Informationen werden über eine WMI-Schnittstelle (Windows-Verwaltungsinstrumentation) verfügbar gemacht, sodass diese von tragbaren Lesegeräten genutzt werden können. Indem sie die Zuverlässigkeitsanalysekomponente über eine WMI-Schnittstelle verfügbar machen, können Entwickler ihre Anwendungen überwachen und analysieren und auf diese Weise die Zuverlässigkeit und Leistung verbessern.

Windows 7 verwendet die integrierte Zuverlässigkeitsanalyse Komponente, um einen Zuverlässigkeits Index zu berechnen, der Informationen über die allgemeine Systemnutzung und Stabilität im Zeitverlauf bereitstellt. Mithilfe der Zuverlässigkeitsanalysekomponente werden zudem alle wichtigen Systemänderungen nachverfolgt, die sich auf die Stabilität auswirken können, z. B. Windows-Updates und Anwendungsinstallationen. Sie können das Snap-in "Zuverlässigkeits Monitor" verwenden, um Trends im Zuverlässigkeits Index Ihres Systems zu erkennen, die mit diesen potenziell destabilierenden Ereignissen korreliert sind, sodass es einfach ist, eine Zuverlässigkeits Änderung direkt zu einem bestimmten Ereignis zu verfolgen. (Siehe [mountvhd-Funktion](/previous-versions/windows/desktop/msvs/mountvhd).)

 

 