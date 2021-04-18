---
description: Die RealTimeStylus-Klasse ermöglicht es Ihnen, mit dem Datenstrom vom Tablettstift zu interagieren. Wenn Sie mit dem Datenstrom interagieren möchten, fügen Sie der Anwendung ein RealTimeStylus-Objekt hinzu, und fügen Sie dem RealTimeStylus-Objekt Plug-Ins hinzu.
ms.assetid: 4009aeac-d290-4ea5-a6f5-199010acc84d
title: Arbeiten mit den StylusInput-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676752f242aa428b583390d7c3d38c952b4c0edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368067"
---
# <a name="working-with-the-stylusinput-apis"></a>Arbeiten mit den StylusInput-APIs

Die [**RealTimeStylus**](realtimestylus-class.md) -Klasse ermöglicht es Ihnen, mit dem Datenstrom vom Tablettstift zu interagieren. Wenn Sie mit dem Datenstrom interagieren möchten, fügen Sie der Anwendung ein **RealTimeStylus** -Objekt hinzu, und fügen Sie dem **RealTimeStylus** -Objekt Plug-Ins hinzu.

Die Plug-Ins können die Daten ändern, die mit in-Air-Paketen, tablettdown-, Paket-und tablettstiftbenachrichtigungs Methoden verknüpft sind. Mit den Plug-Ins können die in-Air-Pakete und Benachrichtigungs Methoden für Pakete abgebrochen werden. Die Plug-Ins können dem Stream auch Anwendungsdaten in Form von [CustomStylusData](/previous-versions/ms575208(v=vs.100)) -Objekten hinzufügen. Die folgende Liste enthält Ideen für gängige Kategorien von Plug-ins, die Sie möglicherweise verwenden oder erstellen möchten.

-   Filter-Plug-in: ein Objekt, das Daten im Tablet Pen-Datenstrom selektiv entfernt oder abbricht.
-   Modifiziererplug-in: ein Objekt, das Daten im Tablet Pen-Datenstrom selektiv ändert.
-   Dynamic-Renderer-Plug-in: ein Objekt, das die Tablet Pen-Daten in Echtzeit anzeigt, wie Sie vom [**RealTimeStylus**](realtimestylus-class.md) -Objekt verarbeitet werden. Für Ereignisse wie z. b. eine Formular Aktualisierung könnte das dynamische Renderer-Plug-in oder ein frei Hand Eingabe-Plug-in das frei Handzeichen neu zeichnen.
-   Erkennungs-Plug-in: ein Objekt, das die Bewegung des Tablettstifts für Gesten, Handschrift oder andere Symbole scannt.
-   Ink-Collector-Plug-in: ein Objekt, das vom Tablet Pen Data Stream erstellt und gespeichert wird.
-   Wrapper-Plug-in: ein Plug-in, das als Schnittstelle zwischen dem [**RealTimeStylus**](realtimestylus-class.md) -Objekt und einem anderen Plug-in oder Objekt fungiert, um das Verhalten des Wrapper Objekts zu ändern.

Sowohl Dynamic-Renderer-als auch Freihand-Auflistungs-Plug-Ins können erstellt werden, um Sie in verschiedenen Kontexten zu rendern – z. b. in einer Datei, einem Stream oder einem Anzeigegerät. Frei Hand Eingaben können auch in verschiedenen Formaten gespeichert werden, z. b. in einem [Ink](/previous-versions/aa515768(v=msdn.10)) -Objekt, einer GIF-Datei (angereichert Graphics Interchange Format), einer ISF-Datei (Ink Serialized Format) oder anderen Formaten.

Mit den StylusInput-APIs werden zwei Plug-ins bereitgestellt: die [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) -Klasse und die [**GestureRecognizer**](gesturerecognizer-class.md) -Klasse. Die **DynamicRenderer** -Klasse stellt das grundlegende Rendering der frei Hand Daten in Echtzeit bereit und ist so optimiert, dass Sie eine minimale Auswirkung auf die Leistung haben. Die **GestureRecognizer** -Klasse stellt Gestenerkennung für die [**RealTimeStylus**](realtimestylus-class.md) -Klasse bereit.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Arbeiten mit der RealTimeStylus-Klasse](working-with-the-realtimestylus-class.md)
-   [Plug-ins und die RealTimeStylus-Klasse](plug-ins-and-the-realtimestylus-class.md)
-   [Plug-In-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md)
-   [Implementierungs Hinweise für die StylusInput-APIs](implementation-notes-for-the-stylusinput-apis.md)
-   [Plug-Ins für die frei Hand Erfassung](ink-collection-plug-ins.md)
-   [Plug-Ins für dynamisches Renderer](dynamic-renderer-plug-ins.md)
-   [Erkennungs-Plug-ins](recognizer-plug-ins.md)

 

 
