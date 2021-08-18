---
description: Der Tablet-PC enthält Technologie für die Interaktion mit Tablettstiftdaten während der Datenerfassung.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Zugreifen auf und Bearbeiten von Stifteingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df56b690a8b7459f42e7d692e47dff4e9f1c00330e02cc0c912d7a3ca3dda02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452057"
---
# <a name="accessing-and-manipulating-stylus-input"></a>Zugreifen auf und Bearbeiten von Stifteingaben

Der Tablet-PC enthält Technologie für die Interaktion mit Tablettstiftdaten während der Datenerfassung. Die [**RealTimeStylus-Klasse**](realtimestylus-class.md) ist Teil der Anwendungsprogrammierschnittstellen (API) StylusInput, die Zugriff auf den Tablettstiftdatenstrom bieten. Mit diesen APIs können Sie den Stream unabhängig vom Rendern und Sammeln von Ink-Daten erfassen, unterbrechen und ändern.

Die StylusInput-APIs sind für:

-   Bieten Sie Echtzeitzugriff auf den Tablettstift-Datenstrom.
-   Halten Sie den Ui-Thread (Benutzeroberflächenthread) davon ab, das dynamische Ink-Rendering zu blockieren, indem Sie die Paketdaten im UI-Thread in die Warteschlange einordnen und die Ink-Sammlung als Singlethread erstellen.
-   Erhöhen Sie die Leistung, und senken Sie die allgemeine Threadverwendung mithilfe des [**InkCollector-Objekts,**](inkcollector-class.md) [**des InkOverlay-Objekts,**](inkoverlay-class.md) des [InkPicture-Steuerelements](inkpicture-control-reference.md) oder des [InkEdit-Steuerelements,](inkedit-control-reference.md) um Dies zu erfassen.

Die StylusInput-APIs sind nicht für die Arbeit mit dem [**InkCollector-Objekt,**](inkcollector-class.md) [**dem InkOverlay-Objekt,**](inkoverlay-class.md) dem [InkPicture-Steuerelement](inkpicture-control-reference.md) oder dem [InkEdit-Steuerelement](inkedit-control-reference.md) konzipiert.

Verwenden Sie das [**RealTimeStylus-Objekt,**](realtimestylus-class.md) wenn Sie direkt mit dem Tablettstift-Datenstrom interagieren müssen oder Ihre Anwendung die Echtzeit-Inknung blockieren kann. Verwenden Sie [**das InkCollector-Objekt,**](inkcollector-class.md) [**das InkOverlay-Objekt,**](inkoverlay-class.md) das [InkPicture-Steuerelement](inkpicture-control-reference.md) oder das [InkEdit-Steuerelement,](inkedit-control-reference.md) wenn das Standardverhalten dieser Objekte das von Ihnen benötigte Verhalten bietet.

## <a name="in-this-section"></a>In diesem Abschnitt

In den folgenden Abschnitten werden Elemente der StylusInput-APIs beschrieben:

-   [Architektur der StylusInput-APIs](architecture-of-the-stylusinput-apis.md)
-   [Arbeiten mit den StylusInput-APIs](working-with-the-stylusinput-apis.md)
    -   [Arbeiten mit der RealTimeStylus-Klasse](working-with-the-realtimestylus-class.md)
    -   [Plug-Ins und die RealTimeStylus-Klasse](plug-ins-and-the-realtimestylus-class.md)
    -   [Plug-In-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md)
    -   [Implementierungshinweise für die StylusInput-APIs](implementation-notes-for-the-stylusinput-apis.md)
    -   [Ink-Collection-Plug-Ins](ink-collection-plug-ins.md)
    -   [Dynamic-Renderer-Plug-Ins](dynamic-renderer-plug-ins.md)
    -   [Erkennen von Plug-Ins](recognizer-plug-ins.md)
-   [Überlegungen bei der Verwendung der StylusInput-APIs](considerations-when-using-the-stylusinput-apis.md)
    -   [Entwurfsüberlegungen für die StylusInput-APIs](design-considerations-for-the-stylusinput-apis.md)
    -   [Überlegungen zum Threading für die StylusInput-APIs](threading-considerations-for-the-stylusinput-apis.md)

[Das kaskadierte RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md)

-   [Überlegungen zur Fehlerbehandlung für die StylusInput-APIs](error-handling-considerations-for-the-stylusinput-apis.md)
-   [Überlegungen zur Leistung der StylusInput-APIs](performance-considerations-for-the-stylusinput-apis.md)
-   [Überlegungen zur teilweisen Vertrauenswürdigkeit der StylusInput-APIs](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[RealTimeStylus-Plug-In-Beispiel](realtimestylus-plug-in-sample.md)
</dt> <dt>

[RealTimeStylus Ink Collection Sample](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



