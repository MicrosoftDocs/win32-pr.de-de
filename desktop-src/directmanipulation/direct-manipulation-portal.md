---
description: Mit den APIs für die direkte Bearbeitung können Sie großartige schwenken, Zoomen und ziehen von Benutzeroberflächen erstellen. Zu diesem Zweck verarbeitet er die Berührungs Eingaben für eine Region oder ein Objekt, generiert Ausgabe Transformationen und wendet die Transformationen auf Benutzeroberflächen Elemente an.
ms.assetid: 26358bc5-71e9-40f0-9243-9bddd961a0e5
title: Direkte Bearbeitung
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6db2a50893914dfb25050768f88cb289a1ecf3ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124316"
---
# <a name="direct-manipulation"></a>Direkte Bearbeitung

Mit den APIs für die direkte Bearbeitung können Sie großartige schwenken, Zoomen und ziehen von Benutzeroberflächen erstellen. Zu diesem Zweck verarbeitet er die Berührungs Eingaben für eine Region oder ein Objekt, generiert Ausgabe Transformationen und wendet die Transformationen auf Benutzeroberflächen Elemente an. Sie können die direkte Bearbeitung verwenden, um die Reaktionsfähigkeit zu optimieren und die Latenzzeit zu verringern, indem Sie die Verarbeitung außerhalb der Thread Eingaben, optionale Eingangs Treffer Tests von Off und Eingabe-/Ausgabe-

Jede Anwendung, die direkte Bearbeitung zum Verarbeiten von touchinteraktionen verwendet, zeigt die flüssigen Windows 8-Animationen und Interaktions Feedback Verhalten an, die den [Richtlinien für gängige Benutzerinteraktionen](/windows/uwp/design/input/)entsprechen.

## <a name="developer-audience"></a>Entwicklerzielgruppe

Die direkte Bearbeitungs-API ist für erfahrene Entwickler gedacht, die C/C++ kennen, ein solides Verständnis der [Component Object Model (com)](../com/component-object-model--com--portal.md)haben und mit den Windows-Programmier Konzepten vertraut sind.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Direkte Manipulation wurde in Windows 8 eingeführt. Sie ist in 32-Bit-und 64-Bit-Versionen enthalten.

## <a name="why-use-directmanipulation"></a>Gründe für die Verwendung von directmanipulation

### <a name="handles-interactions-in-a-straightforward-and-consistent-manner"></a>Behandelt Interaktionen auf einfache und konsistente Weise

Die direkte Bearbeitung funktioniert, indem das Verhalten und die Interaktionen für eine Region oder ein Objekt vorab deklariert werden. Beispielsweise wird eine Webseite häufig für Schwenken und Zoom konfiguriert. Zur Laufzeit wird dieser Region/diesem Objekt dann über einen einfachen API-Befehl eine Eingabe zugeordnet. Ab diesem Punkt führt die direkte Manipulation die Verarbeitung der Eingabe, das Anwenden von Einschränkungen und die Persönlichkeit und das Erzeugen der Ausgabe Transformationen durch.

### <a name="build-responsive-touch-applications"></a>Erstellen von reaktionsfähigen Berührungs Anwendungen

Um die Reaktionsfähigkeit zu optimieren und die Latenz zu minimieren, erfolgt die Verarbeitung direkter Manipulationen in einem separaten, unabhängigen Thread aus dem UI-Thread. Folglich können Ausgabe Transformationen parallel zu Aktivitäten im UI-Thread ausgeführt werden. Die UI-Thread Aktivität kann Anwendungslogik, Rendering, Layout und alle anderen Elemente enthalten, die Zyklen für den Prozessor verbrauchen.

### <a name="implementation-flexibility"></a>Implementierungs Flexibilität

Die in Direct Manipulation enthaltenen Schnittstellen bieten umfassende Unterstützung für die Eingabe Behandlung, die Interaktions Erkennung, Feedback Benachrichtigungen und Aktualisierungen der Benutzeroberfläche. Die Schnittstellen enthalten auch Systemdienste wie [directcomposition](../directcomp/directcomposition-portal.md).

## <a name="basic-concepts"></a>Grundlegende Konzepte

Die grundlegendste direkte Manipulations Implementierung besteht aus *Viewports*, *Inhalten* und *Interaktionen*. Der *Viewport* ist eine Region, die Eingaben von Benutzerinteraktionen empfangen und verarbeiten kann. Es ist auch der Bereich des Inhalts, der für den Endbenutzer sichtbar ist. Der *Inhalt* ist das eigentliche Objekt, das Endbenutzer sehen können, und wird als Reaktion auf eine Benutzerinteraktion verschoben bzw. skaliert. Die primären Benutzer *Interaktionen* (auch als *Manipulationen* bezeichnet), die von direkter Bearbeitung unterstützt werden, sind schwenken und Zoomen. Diese Interaktionen wenden eine Übersetzung oder Skalierungs Transformation auf den Inhalt im Viewport an. Mehrere Viewports (mit jeweils eigenem Inhalt) können in einem einzelnen Fenster konfiguriert werden, um eine umfangreiche Benutzeroberfläche zu erstellen.

Diese Abbildung zeigt eine einfache Implementierung der direkten Bearbeitung vor und nach dem schwenken.

![grundlegende Implementierung der direkten Bearbeitung vor und nach dem schwenken.](images/dm-art-1.png)

Während der Initialisierung der direkten Bearbeitung wird ein **dcompdirectmanipulationcompositor** -Objekt instanziiert und der direkten Bearbeitung zugeordnet. Bei diesem Objekt handelt es sich um einen Wrapper um [directcomposition](../directcomp/directcomposition-portal.md), bei dem es sich um die System Komposition handelt. Das-Objekt ist für das Anwenden der Ausgabe Transformationen und das Vorantreiben von visuellen Updates verantwortlich.

Ein Kontakt stellt einen Berührungspunkt dar, der durch die in der [WM/_POINTERDOWN-](../inputmsg/wm-pointerdown.md) Meldung bereitgestellte **pointerid** identifiziert wird. Wenn eine **WM- \_ pointerdown** -Nachricht empfangen wird, ruft die Anwendung [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)auf. Die Anwendung benachrichtigt direkte manipulationinformationen über die Kontakte, die behandelt werden sollen, und über die Viewports, die auf diese Kontakte reagieren sollen. Tastatur-und Maus Eingaben haben besondere **pointerid** -Werte, sodass Sie von direkter Bearbeitung ordnungsgemäß verarbeitet werden können.

In unserem grundlegenden Fall oben, wenn [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) aufgerufen wird, geschieht Folgendes:

- Wenn der Benutzer eine schwenken ausführt, wird eine [WM/_POINTERCAPTURECHANGED-](../inputmsg/wm-pointercapturechanged.md) Meldung an die Anwendung gesendet, um zu benachrichtigen, dass der Kontakt durch direkte Bearbeitung genutzt wurde.
- Wenn der Benutzer die Verschiebung verschiebt, löst der Viewport Update Ereignisse aus, die vom [directcomposition](../directcomp/directcomposition-portal.md) -Wrapper verwendet werden, um visuelle Updates auf den Bildschirm zu überprüfen. Bei einem Benutzer, der sich in einem Viewport bewegt, wird der Inhalt scheinbar reibungslos unter dem Kontakt verschoben.
- Wenn der Benutzer den Kontakt anrichtet, sieht der Benutzer, dass der Inhalt weiter bewegt wird, während er in eine Trägheit-Animation übergeht, und langsam verlangsamt, bis er seine endgültige Ruhe Stelle erreicht.

## <a name="processing-keyboard-and-mouse-input"></a>Verarbeiten der Tastatur-und Maus Eingaben

Die direkte Bearbeitung ermöglicht das manuelle Weiterleiten von Tastatur-und Maus Nachrichten aus dem Anwendungs Benutzeroberflächen Thread über die [**ProcessInput**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-processinput) -API, sodass Sie durch direkte Bearbeitung ordnungsgemäß verarbeitet werden können.

## <a name="directmanipulation-and-the-hwnd"></a>Directmanipulation und HWND

Eine direkte Bearbeitung ist einem Win32-HWND zugeordnet, um Zeiger Eingabe Meldungen für dieses Fenster zu empfangen und zu verarbeiten. Wenn die direkte Bearbeitung Ausgabewerte berechnet, werden asynchrone Rückrufe für die in der Anwendung implementierten com-Objekte (Direct Manipulation [Component Object Model)](../com/component-object-model--com--portal.md) vorgenommen. Diese Rückrufe informieren die Anwendung über die Transformation, die auf die Objekte angewendet wurde. Die direkte Bearbeitung wird auf dem angegebenen HWND aktiviert, indem " [**aktivieren**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-activate)" aufgerufen wird.

## <a name="supporting-documentation"></a>Unterstützende Dokumentation

- [Viewports und Inhalt](directmanipulation-viewports-and-content.md)
- [Verwenden mehrerer Viewports in directmanipulation](directmanipulation-multiple-vieports.md)
- [Verarbeiten von Eingaben mit directmanipulation](directmanipulation-processing-input-with-directmanipulation.md)
- [Kompositions Modul](directmanipulation-composition-engine.md)
- [Verweis auf direkte Manipulation](direct-manipulation-reference.md)

- [Build 2013: WCL-022: machen Sie Ihre Desktop-App hervorragend mit berühren, Maus und Stift](https://channel9.msdn.com/Events/Build/2013/4-022)
- [Beispiel für die Verarbeitung von Berührungs Eingaben mit direkter Manipulation](https://github.com/microsoft/Windows-classic-samples/tree/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/TouchInputDirectManipulation)
