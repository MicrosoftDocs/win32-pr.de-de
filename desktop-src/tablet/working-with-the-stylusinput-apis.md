---
description: Mit der RealTimeStylus-Klasse können Sie mit dem Datenstrom aus dem Tablettstift interagieren. Um mit dem Datenstrom zu interagieren, fügen Sie Ihrer Anwendung ein RealTimeStylus-Objekt und dem RealTimeStylus-Objekt Plug-Ins hinzu.
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: Arbeiten mit den StylusInput-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 143cb885cda16542a65aa096cdf95eb8a187b4f760a916a895887737ec63d7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842840"
---
# <a name="working-with-the-stylusinput-apis"></a>Arbeiten mit den StylusInput-APIs

Mit [**der RealTimeStylus-Klasse**](realtimestylus-class.md) können Sie mit dem Datenstrom aus dem Tablettstift interagieren. Um mit dem Datenstrom zu interagieren, fügen Sie Ihrer Anwendung ein **RealTimeStylus-Objekt** und dem **RealTimeStylus-Objekt Plug-Ins** hinzu.

Die Plug-Ins können die Daten ändern, die den Benachrichtigungsmethoden in der Luft, dem Stift, den Paketen und dem Stift zugeordnet sind. Die Plug-Ins können die Benachrichtigungsmethoden für Pakete und Pakete in der Luft abbrechen. Die Plug-Ins können dem Stream auch Anwendungsdaten in Form von [CustomStylusData-Objekten](/previous-versions/ms575208(v=vs.100)) hinzufügen. Die folgende Liste enthält Ideen für allgemeine Kategorien von Plug-Ins, die Sie verwenden oder erstellen möchten.

-   Filter-Plug-In: Ein Objekt, das Daten im Tablettstiftdatenstrom selektiv entfernt oder abbricht.
-   Modifizierer-Plug-In: Ein Objekt, das Daten im Tablettstiftdatenstrom selektiv ändert.
-   Plug-In für dynamische Renderer: Ein Objekt, das die Tablettstiftdaten in Echtzeit anzeigt, während sie vom [**RealTimeStylus-Objekt verarbeitet**](realtimestylus-class.md) werden. Später kann das Plug-In für den dynamischen Renderer oder ein Ink-Sammlungs-Plug-In die Ink-Datei für Ereignisse wie eine Formularaktualisierung neu gezeichnet werden.
-   Recognizer-Plug-In: Ein Objekt, das die Bewegung des Tablettstifts auf Gesten, Handschrift oder andere Glyphen überprüft.
-   Ink-Collector-Plug-In: Ein Objekt, das aus dem Tablettstiftdatenstrom Ink erstellt und speichert.
-   Wrapper-Plug-In: Ein Plug-In, das als Schnittstelle zwischen dem [**RealTimeStylus-Objekt**](realtimestylus-class.md) und einem anderen Plug-In oder -Objekt fungiert, um das Verhalten des umschlossenen Objekts zu ändern.

Sowohl Dynamic-Renderer- als auch Ink-Collection-Plug-Ins können für das Rendern in verschiedenen Kontexten erstellt werden, z. B. in einer Datei, einem Stream oder einem Anzeigegerät. Ink kann auch in verschiedenen Formaten gespeichert werden, z. B. in einem [Ink-Objekt,](/previous-versions/aa515768(v=msdn.10)) in einer FOR Graphics Interchange Format-Datei (GIF), in einer ISF-Datei (serialisiertes Freihandformat) oder in anderen Formaten.

Mit den StylusInput-APIs werden zwei Plug-Ins bereitgestellt: die [**DynamicRenderer-Klasse**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) und die [**GestureRecognizer-Klasse.**](gesturerecognizer-class.md) Die **DynamicRenderer-Klasse** bietet grundlegendes Rendering der Ink-Daten in Echtzeit und ist optimiert, um eine minimale Auswirkung auf die Leistung zu haben. Die **GestureRecognizer-Klasse** bietet Gestenerkennung für die [**RealTimeStylus-Klasse.**](realtimestylus-class.md)

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Arbeiten mit der RealTimeStylus-Klasse](working-with-the-realtimestylus-class.md)
-   [Plug-Ins und die RealTimeStylus-Klasse](plug-ins-and-the-realtimestylus-class.md)
-   [Plug-In-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md)
-   [Implementierungshinweise für die StylusInput-APIs](implementation-notes-for-the-stylusinput-apis.md)
-   [Ink-Collection-Plug-Ins](ink-collection-plug-ins.md)
-   [Dynamic-Renderer-Plug-Ins](dynamic-renderer-plug-ins.md)
-   [Erkennen von Plug-Ins](recognizer-plug-ins.md)

 

 
