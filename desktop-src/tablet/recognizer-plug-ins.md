---
description: Ein Recognizer-Plug-In ist ein Objekt, das die Bewegung des Tablettstifts auf Gesten, Handschrift oder andere Objekte überwacht.
ms.assetid: 764a327e-1da0-487f-9245-b6a4f3f43502
title: Erkennen von Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b64f8f9b63cdbdc7309e7d9bd303ecce7a6b59b2e3b3c0cde976d1d6eefdf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091525"
---
# <a name="recognizer-plug-ins"></a>Erkennen von Plug-Ins

Ein Recognizer-Plug-In ist ein Objekt, das die Bewegung des Tablettstifts auf Gesten, Handschrift oder andere Objekte überwacht.

## <a name="system-gestures"></a>Systemgesten

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) erkennt Systemgesten. Das **RealTimeStylus-Objekt** fügt der [StylusQueues-Warteschlange](/previous-versions/ms824786(v=msdn.10)) ein [SystemGestureData-Objekt](/previous-versions/ms824019(v=msdn.10)) als Antwort auf die Daten hinzu, die die Geste beenden, z. B. ein [StylusUpData-Objekt](/previous-versions/ms824057(v=msdn.10)) für [systemGesture](/previous-versions/bb345349(v=vs.100)). Weitere Informationen finden Sie unter [Plug-In-Daten und realTimeStylus-Klasse.](plug-in-data-and-the-realtimestylus-class.md)

## <a name="the-gesturerecognizer-object"></a>Das GestureRecognizer-Objekt

Das [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) implementiert die [**Schnittstellen IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) und [**IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) Das **GestureRecognizer-Objekt** erkennt Anwendungsgesten. Intern verwendet das **GestureRecognizer-Objekt** die Microsoft-Gestenerkennung, um die Gestenerkennung durchzuführen.

Wenn das [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) eine Geste erkennt, fügt es der [StylusQueues-Warteschlange](/previous-versions/ms824786(v=msdn.10)) benutzerdefinierte Stiftdaten als Antwort auf das [StylusUpData-Objekt](/previous-versions/ms824057(v=msdn.10)) für den Strich hinzu. Die [CustomDataId-Eigenschaft](/previous-versions/ms824748(v=msdn.10)) des [CustomStylusData-Objekts](/previous-versions/ms575208(v=vs.100)) wird auf den [GestureRecognitionDataGuid-Wert](/previous-versions/ms826344(v=msdn.10)) festgelegt, und die [Data-Eigenschaft](/previous-versions/ms824749(v=msdn.10)) des CustomStylusData-Objekts enthält ein [GestureRecognitionData-Objekt.](/previous-versions/ms824594(v=msdn.10))

Das folgende Diagramm veranschaulicht, wie das [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) den Tablettstiftdaten Daten hinzufügt.

![Abbildung des GestureRecognizer-Datenflusses](images/c4c77c33-deee-49d0-84bc-12612575ec66.gif)

In diesem Diagramm stellt der Kreis mit dem Buchstaben "SD" ein [StylusDownData-Objekt](/previous-versions/ms824107(v=msdn.10)) dar, und die Kreise mit dem Buchstaben "P" stellen [PacketsData-Objekte](/previous-versions/ms824590(v=msdn.10)) dar, die bereits der Ausgabewarteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) hinzugefügt wurden und noch nicht an die asynchrone Plug-In-Sammlung gesendet wurden. Der Kreis mit dem Buchstaben "SU" stellt ein [StylusUpData-Objekt](/previous-versions/ms824057(v=msdn.10)) dar, das derzeit vom **RealTimeStylus-Objekt** verarbeitet wird. Sie wird an die synchrone Plug-In-Sammlung gesendet und dann in der Ausgabewarteschlange platziert. Die Kreise mit dem Buchstaben "GR" stellen benutzerdefinierte Stiftdaten dar, die der Eingabewarteschlange vom [**GestureRecognizer-Plug-In**](gesturerecognizer-class.md) als Reaktion auf die dem "SU" zugeordnete Stifteingabebenachrichtigung hinzugefügt werden. Die benutzerdefinierten Tablettstiftdaten mit dem Buchstaben "GR" werden dann an die synchronen Plug-Ins und dann an die Ausgabewarteschlange übergeben, bevor die nächsten Tablettstiftdaten verarbeitet werden. Der leere Kreis stellt die Position in der Ausgabewarteschlange dar, an der zukünftige Tablettstiftdaten hinzugefügt werden.

Standardmäßig erkennt das [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) nur Gesten mit nur einem Strich. Das **GestureRecognizer-Objekt** kann jedoch so festgelegt werden, dass Es multistroke-Gesten erkennt. Bei Gesten mit mehreren Tastatureingaben wird das [CustomStylusData-Objekt](/previous-versions/ms575208(v=vs.100)) der [Warteschlange StylusQueues](/previous-versions/ms824786(v=msdn.10)) als Reaktion auf das [StylusUpData-Objekt](/previous-versions/ms824057(v=msdn.10)) für den letzten Strich der Geste hinzugefügt. Wenn Sie Gesten mit mehreren Strichen erkennen, erhalten Sie möglicherweise Benachrichtigungen zu überlappenden Strichsätzen. Beispielsweise können der erste und zweite Strich zusammen als eine Geste erkannt werden, und der zweite Strich allein kann als Geste erkannt werden. Weitere Informationen zur Multistroke-Gestenerkennung finden Sie unter **der GestureRecognizer-Klasse** und der [MaxStrokeCount-Eigenschaft.](/previous-versions/ms826053(v=msdn.10))

Wenn Sie das [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) für die Multistroke-Gestenerkennung verwenden, erzielen Sie möglicherweise eine optimale Leistung, indem Sie ein kaskadiertes [**RealTimeStylus-Modell**](realtimestylus-class.md) verwenden und das **GestureRecognizer-Objekt** an das sekundäre **RealTimeStylus-Objekt** anfügen. Weitere Informationen zum kaskadierenden **RealTimeStylus-Modell** finden Sie unter [Das kaskadierte RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).

### <a name="special-considerations"></a>Besondere Überlegungen

In der folgenden Liste werden weitere Punkte beschrieben, die bei der Verwendung des [**GestureRecognizer-Objekts zu berücksichtigen**](gesturerecognizer-class.md) sind.

-   Sie sollten ein [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) nicht an mehr als ein [**RealTimeStylus-Objekt**](realtimestylus-class.md) anfügen. Sobald zwei **RealTimeStylus-Objekte** aktiviert sind, an die das **GestureRecognizer-Objekt** angefügt ist, geschieht Folgendes.
    -   Das [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) löst als Reaktion auf den zweiten Aufruf seiner RealTimeStylusEnabled-Methode eine Ausnahme aus.
    -   Das zweite [**RealTimeStylus-Objekt,**](realtimestylus-class.md) das aktiviert wurde, generiert ein [ErrorData-Objekt](/previous-versions/ms824740(v=msdn.10)) und benachrichtigt die verbleibenden Plug-Ins in den Plug-In-Auflistungen über den Fehler.
    -   Das [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) beendet die Erkennung von Gesten.
-   Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) löst eine Ausnahme aus, wenn seine [AddCustomStylusDataToQueue-Methode](/previous-versions/ms825761(v=msdn.10)) mit dem *guid-Parameter* aufgerufen wird, der auf den global eindeutigen Bezeichner (Globally Unique Identifier, GUID) [Microsoft.StylusInput.GestureRecognizer.GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) festgelegt ist.
-   Das [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) wird als Component Object Model-Wrapper (COM) implementiert, und Sie können die [**IStylusSyncPlugin-**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) oder [**IStylusAsyncPlugin-Schnittstellenmethoden**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) nicht direkt aufrufen. Weitere Informationen zur COM-Implementierung und zum [**RealTimeStylus-Objekt**](realtimestylus-class.md) finden Sie unter [Implementierungshinweise für die StylusInput-APIs.](implementation-notes-for-the-stylusinput-apis.md)

## <a name="custom-gesture-recognition"></a>Benutzerdefinierte Gestenerkennung

Sie können ein benutzerdefiniertes Recognizer-Plug-In erstellen, das Handschrift, Gesten oder andere Objekte erkennt, indem Sie:

-   Übergeben der Strichinformationen an ein vorhandenes [Recognizer-Objekt](/previous-versions/ms829434(v=msdn.10)) und Verwenden der [AddCustomStylusDataToQueue-Methode](/previous-versions/ms825761(v=msdn.10)) zum Hinzufügen der Ergebnisse zum Tablettstiftdatenstrom.
-   Durchführen der Erkennung in Ihrem Plug-In und Verwenden der [AddCustomStylusDataToQueue-Methode,](/previous-versions/ms825761(v=msdn.10)) um die Ergebnisse dem Tablettstiftdatenstrom hinzuzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsgesten](application-gestures.md)
</dt> <dt>

[Systemgesten](system-gestures.md)
</dt> <dt>

[Zeitachse von Mausnachrichten und Systemereignissen](timeline-of-mouse-messages-and-system-events.md)
</dt> </dl>

 

 
