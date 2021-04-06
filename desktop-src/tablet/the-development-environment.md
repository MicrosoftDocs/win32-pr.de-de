---
description: Sie benötigen keinen Tablet PC, um Tablet PC-Anwendungen zu entwickeln, aber Sie benötigen einen persönlichen Computer, der die weiter unten in diesem Thema aufgeführte Software ausführen kann.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: Die Entwicklungsumgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefa29a518beaf21aa8b2457abf17d9581075f73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960853"
---
# <a name="the-development-environment"></a>Die Entwicklungsumgebung

Sie benötigen keinen Tablet PC, um Tablet PC-Anwendungen zu entwickeln, aber Sie benötigen einen persönlichen Computer, der die weiter unten in diesem Thema aufgeführte Software ausführen kann.

Es wird dringend empfohlen, dass Sie die Anwendung auf einem echten Tablet PC testen, um sicherzustellen, dass alle Unterschiede in der Hardware (z. b. der höherer Auflösungs-Digitalisierer) berücksichtigt werden.

Ein typisches, minimales Entwicklungssystem besteht aus der folgenden Hardware und Software.

## <a name="hardware"></a>Hardware

-   8 MB Festplatten Speicherplatz für eine komplette Installation.
-   Ein Zeigegerät für die Eingabe. Dazu zählen Geräte wie z. b. eine Maus, ein externes Tablet oder ein Tablet PC mit einem versteckten Digitalisierer.

HID steht für Eingabegeräte, einem Standard für Eingabegeräte. Nicht-HID-kompatible Digitalisierungen werden wie eine normale Maus behandelt, während HID-kompatible Digitalisierer eine höhere Auflösung und mehr Metadaten für Striche, wie z. b. Druck, haben, die auf Tablet PC-Hardware installiert sind.

## <a name="software"></a>Software

Zum Entwickeln von Tablet PC-Anwendungen können folgende Betriebssysteme verwendet werden:

-   Windows 7
-   Windows Vista
-   Windows Server 2008
-   Windows XP Tablet PC Edition 2005
-   Windows Server 2003
-   Windows XP Professional

Außerdem benötigen Sie:

-   Visual Studio Version 6 mit Service Pack 5, Visual Studio .net oder Visual Studio .net 2005
-   Microsoft Internet Explorer 6 oder höher (empfohlen)

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a>Details zum entwickeln auf nicht Tablet PC-SKUs von Windows

Die Komponenten der Tablet PC-Plattform können unter Windows XP Professional mit Service Pack 2 oder Windows Server 2003 installiert werden. Unter diesen Betriebssystemen kann die Anwendung frei Hand Eingaben mit der [**InkCollector**](inkcollector-class.md) -Klasse erfassen und getestet und gedeppt werden. Es ist jedoch keine Erkennung verfügbar, es sei denn, Sie installieren auch das Microsoft Windows XP Tablet PC Edition 2005-Erkennungs Paket. Sie können dieses Paket aus dem Download Center auf MSDN herunterladen.

Nachdem Sie die Windows SDK auf einem Windows XP Professional-oder Windows Server 2003-System installiert haben, verfügen Sie über alle Entwicklungsdateien, die zum Erstellen von frei Hand Anwendungen benötigt werden (z. b. "msink AUT. h" für einen com-Entwickler). Es ist jedoch nicht möglich, die Anwendung auf diesem System auszuführen oder zu debuggen, bis Sie die Laufzeitdateien installieren. Im Fall eines com-Entwicklers müssen inkobj.dll beispielsweise installiert und registriert sein. Da Sie sich nicht auf einem System befinden, auf dem diese Platt Formdateien vorhanden sind, müssen Sie die Tablet PC-Platt Form Komponenten aus dem verteilbaren Mergemodul "mstpcrt. msm" installieren, um die Laufzeitdateien auf Ihrem System zu erhalten.

Die einfachste Möglichkeit, die Platt Form Laufzeiten zu Entwicklungszwecken auf einem Windows XP Professional-oder Windows 2000-System zu installieren, ist das Kompilieren des Beispiel-Setup-Projekts, das mit den Beispielen für mobile PCs und Tablet PCs bereitgestellt wird, und die Bereitstellung auf dem Entwicklungs Computer.

> [!Note]  
> Windows Vista und Windows XP Tablet PC Edition 2005 verfügen bereits über die installierten Platt Form Komponenten, sodass keine zusätzlichen Schritte zum Ausführen und Debuggen von Tablet PC-Anwendungen erforderlich sind.

 

Die Steuerelemente [InkEdit](inkedit-control-reference.md) und [InkPicture](inkpicture-control-reference.md) können zum Erfassen von frei Hand Eingaben auf Windows 2000 mit Service Pack 4 oder Windows XP Professional mit Service Pack 2 verwendet werden, wenn die Tablet PC-Platt Form Komponenten durch die Installation der Tablet PC SDK-Version 1,7 vorhanden sind. Sie können jedoch keine Freihand auf nicht Tablet PC-Systemen sammeln, auf denen die Tablet PC-Platt Form Komponenten nicht installiert

Der Windows SDK stellt alle erforderlichen Komponenten zum Entwickeln von Tablet PC-Anwendungen auf nicht-Tablet-SKUs von Windows bereit. Legen Sie den folgenden **DWORD** -Registrierungsschlüssel auf 1 fest, um frei Hand Eingaben für nicht Tablet-SKUs von Windows zu erfassen:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

Dieser Schlüssel ist nur für Entwicklungszwecke vorgesehen.

 

 



