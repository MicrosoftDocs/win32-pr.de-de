---
title: Intuitive Benutzererfahrung
description: Zum ersten Mal ermöglicht Windows 7 Entwicklern und ihren Endbenutzern, ihre Computer durch Berühren des Bildschirms zu steuern.
ms.assetid: cf5be4d6-4284-43e3-86ba-293c4513b477
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14157066225fcf0cbec6b3df5a263be606419eed1ce4fc799d07da6379035ced
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032037"
---
# <a name="intuitive-user-experience"></a>Intuitive Benutzererfahrung

Zum ersten Mal ermöglicht Windows 7 Entwicklern und ihren Endbenutzern, ihre Computer durch Berühren des Bildschirms zu steuern. Touch- und Multi-Touch-Features bieten benutzern eine natürliche, intuitive Möglichkeit, mit PCs zu interagieren. Die Entwicklerplattform enthält Gesten-APIs auf hoher Ebene sowie Touchnachrichten und Toucheingabe-APIs auf niedriger Ebene. Die Benutzeroberflächenelemente der obersten Ebene, z. B. das *Startmenü* und die *Taskleiste,* haben größere Ziele als vorherige Windows-Releases, wodurch sie einfacher mit einem Finger anstelle einer Maus ausgewählt werden können. Visuelles Feedback wird zum Tippen und Doppeltippen bereitgestellt. Windows Explorer und Windows Internet Explorer 8 sind berührungsfreundliche und einfach in Windows 7-Anwendungen integriert.

## <a name="multi-touch-gestures-and-manipulation-and-inertia-apis"></a>Multi-Touch-Gesten sowie Manipulations- und Trägheits-APIs

Windows 7 features improved touch and gesture support (Verbesserte Unterstützung von Touch- und Gestenfunktionen), mit denen Entwickler schnell und einfach einzigartige Anwendungserfahrungen erstellen können, die über einfaches Zeigen, Klicken und Ziehen mit der Maus hinausgehen. Die neuen Multi-Touch-APIs unterstützen umfangreiche Gesten wie Schwenken, Zoomen und Drehen. Alle Gesten bieten direktes visuelles Feedback und interagieren auf natürliche und intuitive Weise mit zugrunde liegenden Inhalten. Beispielsweise iert eine Zoomgeste die Ansicht an der Position der Geste. Toucheingabe-APIs auf niedrigerer Ebene sind auch für benutzerdefinierte Gestendefinitionen und erweiterte Touch-Response-Funktionen verfügbar. Windows 7 stellt eine Entwicklungsplattform bereit, die Entwicklern die Tools bietet, die sie benötigen, um kreative Anwendungen für Multi-Touch-Eingabegeräte zu entwickeln, indem Benutzereingaben von Multi-Touch-Geräten verarbeitet und die Benutzeroberfläche verbessert werden. Das Ergebnis sind intuitivere Umgebungen, die Innovationen bei der PC-Interaktion ermöglichen.

Windows 7 bietet auch Plattformunterstützung für die Objektbearbeitung und Trägheitsverarbeitung. Mit einem funktionsreichen Satz von Manipulationsfunktionen können Sie mehrere Objekte gleichzeitig und mit sehr feiner Granularität strecken, ihre Größe ändern oder sie drehen. Beispielsweise können mehrere digitale Fotos mithilfe von gestenbasierten Gesten in einer einzelnen Sitzung zugeschnitten, in der Größe geändert und gedreht werden.

Windows 7 enthält Trägheits-APIs, die Trägheit simulieren, wenn Objekte verschoben werden, und hand in Hand mit den Manipulations-APIs arbeiten. Beispielsweise können Sie in einer Fotoanwendung die Bearbeitungs-APIs verwenden, um Benutzern das Drehen, Ändern der Größe und Verschieben von Fotos zu ermöglichen. Wenn ein Benutzer ein Foto "wirf", bieten die Trägheits-APIs eine natürliche Interaktion und ermöglichen es dem Foto, an einen Stopp zu ziehen oder von den Rahmen des Fensters der Anwendung zu springen. (Siehe [Windows Touch-Programmierhandbuch](../wintouch/programming-guide.md) und [Windows Touch: Entwicklerressourcen](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch).)

## <a name="single-finger-panning"></a>Single-Finger Panning

In vielen gängigen Anwendungen sind Touchfunktionen für die Navigation nützlicher als für die Textauswahl. Mit erweiterten Touch-APIs kann die Anwendung eines Entwicklers das Schwenken statt ziehen aktivieren. Wenn Sie beispielsweise eine Anwendung erstellt haben, die Multi-Touch-Gesten für Benutzer verwendet, die Musik spielen, können Sie diesen Benutzern erlauben, einfach einen Finger nach oben oder unten zu bewegen, um die Lautstärke anzupassen, Die Musik zu ändern oder eine Datei herunterzuladen. Es ist kein Bildlauf erforderlich.

Windows 7 bietet Entwicklern, die anwendungen für PCs der nächsten Generation erstellen möchten, endlose Möglichkeiten. Das Beste daran ist, dass die Überprüfung auf Scrollleisten und die Implementierung der Schwenksemantik schwierig ist. Anwendungen erhalten auch einen vielfältigeren Satz von Ereignissen und Feedback zur benutzerdefinierten Steuerung von Gesten als in früheren Versionen von Windows. (Siehe [Improving the Single-Finger Panning Experience](../wintouch/improving-the-single-finger-panning-experience.md).)

## <a name="raw-touch-input-data"></a>Unformatierte Toucheingabedaten

In Windows 7 werden neue Toucheingaben durch Interaktionsmodelle ermöglicht, die auf Toucheingabenachrichten auf niedrigerer Ebene zugreifen und benutzerdefinierte Antworten auf Kombinationen von Touchnachrichten bereitstellen. Die Plattform unterstützt den Empfang von rohen Toucheingabedaten für Szenarien wie Multi-Touch-Zeichenanwendungen und benutzerdefinierte Gesten innerhalb einer Anwendung. Sie können die Plattformunterstützung für Touch-Touch verwenden oder Ihre eigenen ursprünglichen Multi-Touch-Erfahrungen erstellen. (Siehe [WM \_ TOUCH Message](../wintouch/wm-touchdown.md).)

 

 