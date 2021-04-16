---
description: Ein Erkennungs-Plug-in ist ein Objekt, das die Bewegung des Tablettstifts für Gesten, Handschrift oder andere Objekte überwacht.
ms.assetid: 764a327e-1da0-487f-9245-b6a4f3f43502
title: Erkennungs-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf3ac866a211a78e2d8f347e89ca20a1906f436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562266"
---
# <a name="recognizer-plug-ins"></a>Erkennungs-Plug-ins

Ein Erkennungs-Plug-in ist ein Objekt, das die Bewegung des Tablettstifts für Gesten, Handschrift oder andere Objekte überwacht.

## <a name="system-gestures"></a>System Gesten

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt erkennt System Gesten. Das **RealTimeStylus** -Objekt fügt der [StylusQueues](/previous-versions/ms824786(v=msdn.10)) -Warteschlange ein [SystemGestureData](/previous-versions/ms824019(v=msdn.10)) -Objekt als Reaktion auf die Daten hinzu, die die Geste beenden, wie z. b. ein [StylusUpData](/previous-versions/ms824057(v=msdn.10)) -Objekt für die [System Bewegung](/previous-versions/bb345349(v=vs.100)). Weitere Informationen finden Sie unter [Plug-in-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md).

## <a name="the-gesturerecognizer-object"></a>Das GestureRecognizer-Objekt

Das [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt implementiert die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Schnittstelle und die [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle. Das **GestureRecognizer** -Objekt erkennt Anwendungs Gesten. Intern verwendet das **GestureRecognizer** -Objekt die Microsoft-Gestenerkennung, um Gestenerkennung auszuführen.

Wenn das [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt eine Geste erkennt, fügt es der [StylusQueues](/previous-versions/ms824786(v=msdn.10)) -Warteschlange benutzerdefinierte Tablettstiftdaten als Reaktion auf das [StylusUpData](/previous-versions/ms824057(v=msdn.10)) -Objekt für den Strich hinzu. Die [CustomDataId](/previous-versions/ms824748(v=msdn.10)) -Eigenschaft des [CustomStylusData](/previous-versions/ms575208(v=vs.100)) -Objekts ist auf den [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) -Wert festgelegt, und die [Daten](/previous-versions/ms824749(v=msdn.10)) Eigenschaft des CustomStylusData-Objekts enthält ein [GestureRecognitionData](/previous-versions/ms824594(v=msdn.10)) -Objekt.

Im folgenden Diagramm wird veranschaulicht, wie das [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt den Tablet Pen-Daten Daten hinzufügt.

![Abbildung des GestureRecognizer-Datenflusses](images/c4c77c33-deee-49d0-84bc-12612575ec66.gif)

In diesem Diagramm stellt der Kreis mit dem Text "SD" ein [StylusDownData](/previous-versions/ms824107(v=msdn.10)) -Objekt dar, und die Kreise "P" stellen [packepdata](/previous-versions/ms824590(v=msdn.10)) -Objekte dar, die bereits der Ausgabe Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts hinzugefügt wurden und noch nicht an die asynchrone Plug-in-Auflistung gesendet wurden. Der Kreis mit dem Titel "su" stellt ein [StylusUpData](/previous-versions/ms824057(v=msdn.10)) -Objekt dar, das das **RealTimeStylus** -Objekt gerade verarbeitet. Sie wird an die synchrone Plug-in-Auflistung gesendet und dann in der Ausgabe Warteschlange abgelegt. Die Kreise, die "GR" enthalten, stellen benutzerdefinierte Tablettstiftdaten dar, die der Eingabe Warteschlange durch das [**GestureRecognizer**](gesturerecognizer-class.md) -Plug-in als Antwort auf die tablettstiftbenachrichtigung "su" hinzugefügt werden. Die benutzerdefinierten Tablettstiftdaten, die "GR" aufweisen, werden dann an die synchronen Plug-ins und dann an die Ausgabe Warteschlange weitergeleitet, bevor die nächsten Tablet Pen-Daten verarbeitet werden. Der leere Kreis stellt die Position in der Ausgabe Warteschlange dar, an der zukünftige Tablet Pen-Daten hinzugefügt werden.

Standardmäßig erkennt das [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt nur Single-Stroke-Gesten. Das **GestureRecognizer** -Objekt kann jedoch so festgelegt werden, dass Zeitgeber-Gesten erkannt werden. Bei Zeitgeber-Gesten wird das [CustomStylusData](/previous-versions/ms575208(v=vs.100)) -Objekt der [StylusQueues](/previous-versions/ms824786(v=msdn.10)) -Warteschlange als Reaktion auf das [StylusUpData](/previous-versions/ms824057(v=msdn.10)) -Objekt für den letzten Strich der Bewegung hinzugefügt. Wenn Sie mehrstufige Gesten erkennen, erhalten Sie möglicherweise Benachrichtigungen für überlappende Sätze von Strichen. Der erste und zweite Strich können z. b. als eine Bewegung erkannt werden, und der zweite Strich selbst kann als Geste erkannt werden. Weitere Informationen zur Erkennung von Zeitgeber-Gesten finden Sie unter der **GestureRecognizer** -Klasse und der [MaxStrokeCount](/previous-versions/ms826053(v=msdn.10)) -Eigenschaft.

Wenn Sie das [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt für die Erkennung von Zeitgeber-Gesten verwenden, erzielen Sie möglicherweise eine optimale Leistung, indem Sie ein kaskadierenden [**RealTimeStylus**](realtimestylus-class.md) -Modell verwenden und das **GestureRecognizer** -Objekt an das sekundäre **RealTimeStylus** -Objekt anfügen. Weitere Informationen zum Cascading **RealTimeStylus** -Modell finden Sie [im Cascaded RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).

### <a name="special-considerations"></a>Besondere Überlegungen

In der folgenden Liste werden andere Punkte beschrieben, die bei Verwendung des [**GestureRecognizer**](gesturerecognizer-class.md) -Objekts zu berücksichtigen sind.

-   Sie sollten ein [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt nicht an mehr als ein [**RealTimeStylus**](realtimestylus-class.md) -Objekt anfügen. Wenn zwei **RealTimeStylus** -Objekte aktiviert sind, an die das **GestureRecognizer** -Objekt angefügt ist, tritt Folgendes auf.
    -   Das [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt löst eine Ausnahme als Reaktion auf den zweiten Aufrufen der RealTimeStylusEnabled-Methode aus.
    -   Das zweite " [**RealTimeStylus**](realtimestylus-class.md) "-Objekt, das aktiviert wurde, generiert ein [ErrorData](/previous-versions/ms824740(v=msdn.10)) -Objekt und benachrichtigt die übrigen Plug-ins in den Plug-in-Auflistungen des Fehlers.
    -   Das [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt beendet das Erkennen von Gesten.
-   Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt löst eine Ausnahme aus, wenn die zugehörige [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) -Methode aufgerufen wird und der *GUID* -Parameter auf [Microsoft. StylusInput. GestureRecognizer. GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) Globally Unique Identifier (GUID) festgelegt ist.
-   Das [**GestureRecognizer**](gesturerecognizer-class.md) -Objekt wird als Component Object Model (com)-Wrapper implementiert, und Sie können die Schnittstellen Methoden [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) oder [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) nicht direkt aufrufen. Weitere Informationen zur com-Implementierung und zum [**RealTimeStylus**](realtimestylus-class.md) -Objekt finden Sie unter [Implementierungs Hinweise für die StylusInput-APIs](implementation-notes-for-the-stylusinput-apis.md).

## <a name="custom-gesture-recognition"></a>Benutzerdefinierte Gestenerkennung

Sie können ein benutzerdefiniertes Erkennungs-Plug-in erstellen, das Handschrift, Gesten oder andere Objekte wie folgt erkennt:

-   Übergeben der Strich Informationen an ein vorhandenes [Erkennungs](/previous-versions/ms829434(v=msdn.10)) Objekt und Verwenden der [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) -Methode zum Hinzufügen der Ergebnisse zum Tablet Pen-Datenstrom.
-   Durchführen der Erkennung innerhalb des Plug-ins und Verwenden der [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) -Methode zum Hinzufügen der Ergebnisse zum Tablet Pen-Datenstrom.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Gesten](application-gestures.md)
</dt> <dt>

[System Gesten](system-gestures.md)
</dt> <dt>

[Zeitachse von Maus Meldungen und System Ereignissen](timeline-of-mouse-messages-and-system-events.md)
</dt> </dl>

 

 
