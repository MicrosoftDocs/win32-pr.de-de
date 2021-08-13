---
description: Sie benötigen keinen Tablet PC, um Tablet PC-Anwendungen zu entwickeln, aber Sie benötigen einen PC, der die weiter unten in diesem Thema aufgeführte Software ausführen kann.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: Die Entwicklungsumgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d6c0de35fa84ec4ee01b3f25aaefec6ab3470fde83161f7aaf2157197bbf1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449213"
---
# <a name="the-development-environment"></a>Die Entwicklungsumgebung

Sie benötigen keinen Tablet PC, um Tablet PC-Anwendungen zu entwickeln, aber Sie benötigen einen PC, der die weiter unten in diesem Thema aufgeführte Software ausführen kann.

Es wird dringend empfohlen, Ihre Anwendung auf einem tatsächlichen Tablet PC zu testen, um sicherzustellen, dass alle Hardwareunterschiede, z. B. der Digitizer mit höherer Auflösung, berücksichtigt werden.

Ein typisches, minimales Entwicklungssystem besteht aus der folgenden Hardware und Software.

## <a name="hardware"></a>Hardware

-   8 MB Festplattenspeicher für eine vollständige Installation.
-   Ein Zeigergerät für die Eingabe. Dies schließt Geräte wie eine Maus, ein externes Tablet oder einen Tablet-PC mit hid-Digitizer ein.

HID steht für Eingabegeräte, ein Standard für Eingabegeräte. Nicht HID-konforme Digitizer werden wie reguläre Maus behandelt, während HID-konforme Digitizer eine höhere Auflösung und mehr Metadaten für Striche haben, z. B. Druck, ähnlich wie bei der Installation auf Tablet PC-Hardware.

## <a name="software"></a>Software

Die folgenden Betriebssysteme können zum Entwickeln von Tablet PC-Anwendungen verwendet werden:

-   Windows 7
-   Windows Vista
-   Windows Server 2008
-   Windows XP Tablet PC Edition 2005
-   Windows Server 2003
-   Windows XP Professional

Außerdem benötigen Sie:

-   Visual Studio Version 6 mit Service Pack 5 oder Visual Studio .NET oder Visual Studio .NET 2005
-   Microsoft Internet Explorer 6 oder höher (empfohlen)

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a>Details zur Entwicklung auf NICHT-Tablet-PC-SKUs von Windows

Die Komponenten der Tablet PC-Plattform können auf Windows XP Professional Service Pack 2 oder Windows Server 2003 installiert werden. Unter diesen Betriebssystemen kann Ihre Anwendung Mit der [**InkCollector-Klasse InkCollector**](inkcollector-class.md) erfassen und getestet und debuggt werden. Es ist jedoch keine Erkennung verfügbar, es sei denn, Sie installieren auch das Microsoft Windows XP Tablet PC Edition 2005 Recognizer Pack. Sie können dieses Paket aus dem Download Center auf MSDN herunterladen.

Nach der Installation des Windows SDK auf einem Windows XP Professional- oder Windows Server 2003-System verfügen Sie über alle Entwicklungsdateien, die zum Erstellen von Ink-Anwendungen erforderlich sind (z. B. msinkaut.h für einen COM-Entwickler). Allerdings können Sie Ihre Anwendung auf diesem System erst ausführen oder debuggen, wenn Sie die Laufzeitdateien installieren. Im Fall eines COM-Entwicklers muss inkobj.dll installiert und registriert werden. Da Sie sich nicht auf einem System befinden, in dem diese Plattformdateien vorhanden sind, müssen Sie die Komponenten der Tablet PC-Plattform aus dem verteilbaren Mergemodul mstpcrt.msm installieren, um die Laufzeitdateien auf Ihrem System zu erhalten.

Die einfachste Möglichkeit, die Plattformlaufzeiten auf einem Windows XP Professional- oder Windows 2000-System für Entwicklungszwecke zu installieren, besteht in der Kompilierung des Beispielsetupprojekts, das mit den Beispielen für mobile pCs und Tablet-PCs bereitgestellt wird, und deren Bereitstellung auf dem Entwicklungscomputer.

> [!Note]  
> Windows Vista und Windows XP Tablet PC Edition 2005 verfügen bereits über die installierten Plattformkomponenten, sodass keine zusätzlichen Schritte zum Ausführen und Debuggen von Tablet PC-Anwendungen erforderlich sind.

 

Die Steuerelemente [InkEdit](inkedit-control-reference.md) und [InkPicture](inkpicture-control-reference.md) können verwendet werden, um Ink-Daten auf Windows 2000 mit Service Pack 4 oder Windows XP Professional mit Service Pack 2 zu erfassen, wenn die Komponenten der Tablet PC-Plattform vorhanden sind, indem Sie das Tablet PC SDK Version 1.7 installieren, aber keine Ink-Daten auf Nicht-Tablet PC-Systemen erfassen, auf denen die Komponenten der Tablet PC-Plattform nicht installiert sind.

Das Windows SDK stellt alle erforderlichen Komponenten zum Entwickeln von Tablet PC-Anwendungen auf Nicht-Tablet-SKUs von Windows. Legen Sie den folgenden **DWORD-Registrierungsschlüssel** auf 1 fest, um Ink auf Nicht-Tablet-SKUs der Windows:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

Dieser Schlüssel ist nur für Entwicklungszwecke vorgesehen.

 

 



