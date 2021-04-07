---
title: Intuitive Benutzer Darstellung
description: Zum ersten Mal ermöglicht Windows 7 Entwicklern und Ihren Endbenutzern, ihre Computer zu steuern, indem Sie den Bildschirm berühren.
ms.assetid: cf5be4d6-4284-43e3-86ba-293c4513b477
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76576883186a77c53256dad7f011b75a7e260ae2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729480"
---
# <a name="intuitive-user-experience"></a>Intuitive Benutzer Darstellung

Zum ersten Mal ermöglicht Windows 7 Entwicklern und Ihren Endbenutzern, ihre Computer zu steuern, indem Sie den Bildschirm berühren. Touch-und Multitouch-Features bieten eine natürliche, intuitive Möglichkeit für Benutzer, mit PCs zu interagieren. Die Entwicklerplattform umfasst Gesten-APIs auf hoher Ebene sowie touchnachrichten auf niedriger Ebene und Toucheingabe-APIs. Die Benutzeroberflächen Elemente der obersten Ebene, wie z. b. das *Startmenü* und die *Taskleiste*, haben größere Ziele als frühere Windows-Versionen, sodass Sie mit einem Finger anstelle der Maus einfacher ausgewählt werden können. Visuelles Feedback wird für tippen und Doppel tippen bereitgestellt. Windows Explorer und Windows Internet Explorer 8 sind sowohl Berührungs freundlich als auch mühelos in Windows 7-Anwendungen integriert.

## <a name="multi-touch-gestures-and-manipulation-and-inertia-apis"></a>Multitouch-Gesten und Bearbeitungs-und Trägheits-APIs

Windows 7 bietet verbesserte Unterstützung für Finger Eingaben und Gesten und ermöglicht Entwicklern die schnelle und einfache Erstellung eindeutiger Anwendungsumgebungen, die über einfache Mauszeiger, klicken und ziehen hinausgehen. Die neuen Multitouch-APIs unterstützen umfangreiche Gesten, wie z. b. Schwenken, Zoomen und drehen. Alle Gesten stellen direktes visuelles Feedback bereit und interagieren mit zugrunde liegenden Inhalten auf natürliche und intuitive Weise. Beispielsweise zentriert eine Zoom Bewegung die Ansicht an der Position der Bewegung. Toucheingabe-APIs auf niedrigerer Ebene sind auch für benutzerdefinierte Gesten Definitionen und erweiterte touchantwortfunktionen verfügbar. Windows 7 bietet eine Entwicklungsplattform, die Entwicklern die Tools bietet, die Sie benötigen, um kreative Anwendungen für Multitouch-Eingabegeräte zu entwickeln, indem Benutzereingaben von Multitouch-Geräten verarbeitet und die Benutzeroberfläche verbessert wird. Das Ergebnis sind intuitiver Umgebungen, die Innovationen bei der PC-Interaktion ermöglichen.

Windows 7 bietet auch Platt Form Unterstützung für Objekt Bearbeitung und Trägheits Verarbeitung. Ein umfangreicher Satz von Bearbeitungsfunktionen ermöglicht es Ihnen, mehrere Objekte gleichzeitig und in sehr feiner Granularität zu Strecken, zu ändern oder zu drehen. Beispielsweise können mehrere digitale Fotos mithilfe von touchbasierten Gesten in einer einzelnen Sitzung abgeschnitten, verkleinert und gedreht werden.

Windows 7 enthält Trägheits-APIs, die Trägheit beim Verschieben von Objekten simulieren und mit den Bearbeitungs-APIs Hand in Hand arbeiten. Beispielsweise können Sie in einer Foto Anwendung die Bearbeitungs-APIs verwenden, um Benutzern das Drehen, Ändern der Größe und das Verschieben von Fotos zu ermöglichen. Wenn ein Benutzer ein Foto "ein-/ausschalten" hat, stellen die Trägheit-APIs eine natürliche Interaktion dar und ermöglichen es, dass das Foto an die Ränder des Fensters der Anwendung angehalten wird. (Weitere Informationen finden Sie unter [Windows-Berührungs Programmier Handbuch](../wintouch/programming-guide.md) und Windows-Fingereingabe [: Entwickler Ressourcen](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch).

## <a name="single-finger-panning"></a>Single-Finger schwenken

In vielen gängigen Anwendungen sind Berührungs Features für die Navigation nützlicher als für die Textauswahl. Mit erweiterten Fingereingabe-APIs kann die Anwendung eines Entwicklers auswählen, dass das Schwenken statt ziehen aktiviert werden soll. Wenn Sie z. b. eine Anwendung erstellt haben, die Multi-Touch-Gesten für Benutzer verwendet, die Musik abspielen, können Sie diesen Benutzern einfach die Möglichkeit geben, einen Finger nach oben oder unten zu verschieben, um das Volume anzupassen, Titel zu ändern oder eine Datei herunterzuladen. Kein Bildlauf erforderlich.

Windows 7 bietet für Entwickler, die an der Erstellung von Anwendungen für PCs der nächsten Generation interessiert sind, unendliche Möglichkeiten. Das beste daran ist, dass die Überprüfung auf Schiebe leisten und die Implementierung der Schwenk Semantik schwierig ist. Anwendungen erhalten außerdem einen umfassenderen Satz von Ereignissen und Feedback für die angepasste Steuerung von Gesten als in früheren Versionen von Windows. (Weitere Informationen finden Sie [unter Verbessern der Single-Finger schwenken](../wintouch/improving-the-single-finger-panning-experience.md).)

## <a name="raw-touch-input-data"></a>Unformatierte Berührungs Eingabedaten

In Windows 7 werden neue Finger Eingaben durch Interaktionsmodelle aktiviert, die auf unter Eingaben auf niedrigerer Ebene zugreifen und angepasste Antworten auf Kombinationen von Berührungs Meldungen bereitstellen. Die Plattform unterstützt den Empfang von Rohdaten Touch-Eingabedaten für Szenarien wie Multitouch-Zeichnungs Anwendungen und benutzerdefinierte Gesten innerhalb einer Anwendung. Sie können die Platt Form Unterstützung für Touch verwenden oder eigene, Multitouch-Funktionen erstellen. (Siehe [WM \_ ](../wintouch/wm-touchdown.md)-Fingereingabe Nachricht.)

 

 