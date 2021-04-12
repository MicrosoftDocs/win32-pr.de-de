---
description: Bietet Zugriff auf die Tablettstiftereignisse von Stift-oder Fingerabdruck-Digitalisierern.
ms.assetid: a239b53c-7fc9-4211-962a-6cfbe0be4e4c
title: RealTimeStylus-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9016779c3165bc8fb6e24e5612901a7fd58435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216973"
---
# <a name="realtimestylus-reference"></a>RealTimeStylus-Referenz

Bietet Zugriff auf die Tablettstiftereignisse von Stift-oder Fingerabdruck-Digitalisierern.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [RealTimeStylus-Klassen und-Schnittstellen](realtimestylus-classes-and-interfaces.md)
-   [RealTimeStylus-Enumerationen](realtimestylus-enumerations.md)
-   [RealTimeStylus-Strukturen](realtimestylus-structures.md)

## <a name="remarks"></a>Bemerkungen

Dieses Objekt implementiert die [**irealtimestylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) -com-Schnittstelle.

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

Sie können Daten aus dem Paketstream in den synchronen und asynchronen Plug-ins des [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekts vollständig steuern, dynamisch rendern, ändern und sogar löschen.

Der Echt Zeit Stift bietet eine Möglichkeit, ein **inksammungsobjekt** zu erstellen, das Single Thread ist und im Thread der Anwendungs Benutzeroberfläche ansässig ist. Dieses **inksammatenobjekt** greift auf die Echt Zeit Stift Daten aus der Warteschlange zu. Ein **InkCollection** -Objekt in Verbindung mit dem Echt Zeit Stift ermöglicht die echtzeitauswahl Bearbeitung und die Echtzeitbearbeitung der gesammelten frei Hand Daten. Weitere Informationen finden Sie unter [zugreifen auf und](accessing-and-manipulating-stylus-input.md)Bearbeiten von Tablettstifteingaben.

Verwenden Sie das [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekt, um direkt mit dem tablettstiftdateistream zu interagieren oder Echt Zeit Eingaben zu blockieren. Verwenden Sie das [**InkCollector-Klassen**](inkcollector-class.md) Objekt, das [**InkOverlay-Klassen**](inkoverlay-class.md) Objekt, das [InkPicture-Steuer](inkpicture-control-reference.md) Element Steuerelement oder das [InkEdit](inkedit-control-reference.md) -Steuerelement, wenn das Standardverhalten dieser Objekte das benötigte Verhalten bereitstellt.

Die Echt Zeit Tablettstiftereignisse befinden sich in einem bestimmten Fenster Handle innerhalb eines bestimmten Fenster Eingabe Rechtecks. Realtimestylusservice kann Tablettstiftdaten an mehrere [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekte senden. Jedes **RealTimeStylus-Klassen** Objekt empfängt Tablettstiftdaten für einen bestimmten Abschnitt eines Fensters, basierend auf der definierten [**irealtimestylus:: windowinputrechteck-Eigenschaft**](/windows/desktop/api/RTSCom/nf-rtscom-irealtimestylus-get_windowinputrectangle) für dieses **RealTimeStylus-Klassen** Objekt. Das **RealTimeStylus-Klassen** Objekt ruft die Tablettstiftdaten ab und verarbeitet diese dann über eine Liste synchroner und asynchroner Plug-ins.

Der Unterschied zwischen den synchronen Plug-ins und den asynchronen Plug-ins liegt in dem Thread, in dem Sie ausgeführt werden, und der aufrufenden Sequenz. Synchrone Plug-ins werden von dem Thread aufgerufen, in dem das [**RealTimeStylus-Klassen**](realtimestylus-class.md) Objekt ausgeführt wird. Jedes Mal, wenn das **RealTimeStylus-Klassen** Objekt instanziiert wird, wird ein Ausführungs Thread instanziiert. Synchrone Plug-ins werden für diesen neuen Thread ausgeführt, der für die Instanz des **RealTimeStylus-Klassen** Objekts instanziiert wird. Asynchrone Plug-ins werden über die Benutzeroberfläche oder den Anwendungs Thread aufgerufen, nachdem der Paketstream von den synchronen Plug-ins verarbeitet und in der Ausgabe Warteschlange gespeichert wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Idynamicrenderer-Schnittstelle**](/windows/desktop/api/RTSCom/nn-rtscom-idynamicrenderer)
</dt> <dt>

[**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)
</dt> <dt>

[**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)
</dt> <dt>

[**Irealtimestylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus)
</dt> </dl>

 

 
