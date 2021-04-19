---
description: Der Tablet PC umfasst Technologien für die Interaktion mit Tablet Pen-Daten, während diese gesammelt werden.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Zugreifen auf und Bearbeiten von Tablettstifteingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333126f195154241333127ec585864bd9d592a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343206"
---
# <a name="accessing-and-manipulating-stylus-input"></a>Zugreifen auf und Bearbeiten von Tablettstifteingaben

Der Tablet PC umfasst Technologien für die Interaktion mit Tablet Pen-Daten, während diese gesammelt werden. Die [**RealTimeStylus**](realtimestylus-class.md) -Klasse ist Teil der StylusInput-API (Application Programming Interfaces), die Zugriff auf den Tablet Pen-Datenstream bereitstellen. Mit diesen APIs können Sie den Stream unabhängig vom Rendern und Sammeln von frei Hand Eingaben erfassen, unterbrechen und ändern.

Die StylusInput-APIs sind für Folgendes konzipiert:

-   Stellen Sie Echtzeitzugriff auf den Tablet Pen-Datenstrom bereit.
-   Sorgen Sie dafür, dass der Benutzeroberflächen Thread das dynamische frei Hand Rendering blockiert, indem die Paketdaten im UI-Thread in die Warteschlange eingereiht werden und die frei Hand Auflistung Single Thread ist.
-   Erhöhen Sie die Leistung, und senken Sie die gesamt Thread Verwendung über das [**InkCollector**](inkcollector-class.md) -Objekt, das [**InkOverlay**](inkoverlay-class.md) -Objekt, das [InkPicture](inkpicture-control-reference.md) -Steuerelement oder das [InkEdit](inkedit-control-reference.md) -Steuerelement, um frei Hand Eingaben

Die StylusInput-APIs sind nicht für die Arbeit mit dem [**InkCollector**](inkcollector-class.md) -Objekt, dem [**InkOverlay**](inkoverlay-class.md) -Objekt, dem [InkPicture](inkpicture-control-reference.md) -Steuerelement oder dem [InkEdit](inkedit-control-reference.md) -Steuerelement konzipiert.

Wenn Sie direkt mit dem Tablettstiftdaten-Datenstrom interagieren müssen oder wenn Ihre Anwendung das Echt Zeit Inking blockieren kann, verwenden Sie das [**RealTimeStylus**](realtimestylus-class.md) -Objekt. Verwenden Sie das [**InkCollector**](inkcollector-class.md) -Objekt, das [**InkOverlay**](inkoverlay-class.md) -Objekt, das [InkPicture](inkpicture-control-reference.md) -Steuerelement oder das [InkEdit](inkedit-control-reference.md) -Steuerelement, wenn das Standardverhalten dieser Objekte das benötigte Verhalten bereitstellt.

## <a name="in-this-section"></a>In diesem Abschnitt

In den folgenden Abschnitten werden die Elemente der StylusInput-APIs beschrieben:

-   [Architektur der StylusInput-APIs](architecture-of-the-stylusinput-apis.md)
-   [Arbeiten mit den StylusInput-APIs](working-with-the-stylusinput-apis.md)
    -   [Arbeiten mit der RealTimeStylus-Klasse](working-with-the-realtimestylus-class.md)
    -   [Plug-ins und die RealTimeStylus-Klasse](plug-ins-and-the-realtimestylus-class.md)
    -   [Plug-In-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md)
    -   [Implementierungs Hinweise für die StylusInput-APIs](implementation-notes-for-the-stylusinput-apis.md)
    -   [Plug-Ins für die frei Hand Erfassung](ink-collection-plug-ins.md)
    -   [Plug-Ins für dynamisches Renderer](dynamic-renderer-plug-ins.md)
    -   [Erkennungs-Plug-ins](recognizer-plug-ins.md)
-   [Überlegungen bei der Verwendung der StylusInput-APIs](considerations-when-using-the-stylusinput-apis.md)
    -   [Entwurfs Überlegungen für die StylusInput-APIs](design-considerations-for-the-stylusinput-apis.md)
    -   [Threading Überlegungen für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md)

[Das Cascaded RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md)

-   [Überlegungen zur Fehlerbehandlung für die StylusInput-APIs](error-handling-considerations-for-the-stylusinput-apis.md)
-   [Überlegungen zur Leistung der StylusInput-APIs](performance-considerations-for-the-stylusinput-apis.md)
-   [Überlegungen zur teilweisen Vertrauenswürdigkeit für die StylusInput-APIs](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Plug-in-Beispiel für RealTimeStylus](realtimestylus-plug-in-sample.md)
</dt> <dt>

[RealTimeStylus Ink Collection-Beispiel](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



