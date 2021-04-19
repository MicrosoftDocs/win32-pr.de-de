---
description: In diesem Thema wird die asynchrone Datenverarbeitung für Media Foundation Transformationen (MFTs) beschrieben.
ms.assetid: d438ffae-fc50-454f-8ce4-2d6676500fff
title: Asynchrone MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a16950cf431eff16f2befb382a77910c49ccb2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343211"
---
# <a name="asynchronous-mfts"></a>Asynchrone MFTs

In diesem Thema wird die asynchrone Datenverarbeitung für Media Foundation Transformationen (MFTs) beschrieben.

> [!Note]  
> Dieses Thema gilt für Windows 7 oder höher.

 

-   [Informationen zu asynchronen MFTs](#about-asynchronous-mfts)
-   [Allgemeine Anforderungen](#general-requirements)
-   [Ereignisse](#events)
-   [ProcessInput](#processinput)
-   [ProcessOutput](#processoutput)
-   [Ernde](#draining)
-   [Lak](#flushing)
-   [Marker](#markers)
-   [Formatieren von Änderungen](#format-changes)
-   [Attribute](#attributes)
-   [Entsperren von asynchronen MFTs](#unlocking-asynchronous-mfts)
-   [Der MFT wird heruntergefahren.](#shutting-down-the-mft)
-   [Registrierung und Enumeration](#registration-and-enumeration)
-   [Zugehörige Themen](#related-topics)

## <a name="about-asynchronous-mfts"></a>Informationen zu asynchronen MFTs

Wenn MFTs in Windows Vista eingeführt wurden, wurde die API für die *synchrone* Datenverarbeitung konzipiert. In diesem Modell wartet der MFT immer entweder auf Eingaben oder wartet auf die Ausgabe.

Denken Sie an einen typischen Video Decoder. Um einen decodierten Frame zu erhalten, ruft der Client [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)auf. Wenn der Decoder über genügend Daten zum Decodieren eines Frames verfügt, werden **ProcessOutput** blockiert, während die MFT den Frame decodiert. Andernfalls gibt **ProcessOutput** **MF_E_TRANSFORM_NEED_MORE_INPUT** zurück, was darauf hinweist, dass der Client [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)aufrufen sollte.

Dieses Modell funktioniert gut, wenn der Decoder alle Decodierungs Vorgänge in einem Thread ausführt. Angenommen, der Decoder verwendet mehrere Threads, um Frames parallel zu decodieren. Um die optimale Leistung zu erzielen, sollte der Decoder immer dann neue Eingaben erhalten, wenn sich ein Decodierungs Thread im Leerlauf Die Rate, mit der Threads Decodierungs Vorgänge ausführen, wird jedoch nicht exakt an den Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) und [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)des Clients angepasst, was dazu führt, dass Threads auf Arbeit warten.

Windows 7 führt die ereignisgesteuerte *asynchrone* Verarbeitung für MFTs ein. Bei diesem Modell sendet ein Ereignis an den Client, wenn die MFT eine Eingabe oder eine Ausgabe benötigt.

## <a name="general-requirements"></a>Allgemeine Anforderungen

In diesem Thema wird beschrieben, wie sich asynchrone MFTs von synchroner MFT unterscheiden. Mit Ausnahme der in diesem Thema genannten, sind die beiden Verarbeitungs Modelle identisch. (Insbesondere ist die Format Aushandlung identisch.)

Ein asynchroner MFT muss die folgenden Schnittstellen implementieren:

-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMF Media Event Generator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**Nicht Herunterfahren**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

## <a name="events"></a>Ereignisse

Ein asynchroner MFT verwendet die folgenden Ereignisse, um den Datenverarbeitungs Status zu signalisieren:



| Ereignis                                                    | BESCHREIBUNG                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [Metransformneedinput](metransformneedinput.md)         | Wird gesendet, wenn die MFT mehr Eingaben akzeptieren kann.                          |
| [Metransformhaveoutput](metransformhaveoutput.md)       | Wird gesendet, wenn die MFT ausgegeben wird.                                     |
| [Metransformdraunvollständig](metransformdraincomplete.md) | Wird gesendet, wenn ein Ausgleichs Vorgang abgeschlossen wird. Siehe [ableiten](#draining). |
| [Metransformmarker](metransformmarker.md)               | Wird gesendet, wenn ein Marker ein Prozess ist. Siehe [Marker](#markers).           |



 

Diese Ereignisse werden out-of-Band gesendet. Es ist wichtig, den Unterschied zwischen in-Band-und Out-of-Band-Ereignissen im Kontext einer MFT zu verstehen.

Der ursprüngliche MFT-Entwurf unterstützt *in-Band-* Ereignisse. Ein in-Band-Ereignis enthält Informationen zum Datenstrom, z. b. Informationen zu einer Formatänderung. Der Client sendet in-Band-Ereignisse durch Aufrufen von [**imftransform::P rocesabvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)an die MFT. Der MFT kann in-Band-Ereignisse in der [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode an den Client zurücksenden. (Insbesondere werden Ereignisse im Member " **Peer Vents** " der [**MFT_OUTPUT_DATA_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) Struktur übermittelt.)

Ein MFT sendet out-of-Band-Ereignisse über die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle wie folgt:

1.  Die MFT implementiert die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle, wie in [Medienereignis Generatoren](media-event-generators.md)beschrieben.
2.  Der Client ruft **IUnknown:: QueryInterface** auf der MFT für die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle auf. Diese Schnittstelle muss von einem asynchronen MFT verfügbar gemacht werden. Synchrone MFTs sollten diese Schnittstelle nicht verfügbar machen.
3.  Vom Client werden [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) und [**imfmediaeventgenerator:: endgetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) aufgerufen, um Out-of-Band-Ereignisse vom MFT zu empfangen.

## <a name="processinput"></a>ProcessInput

Die [**IMF Transform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) -Methode wird wie folgt geändert:

1.  Beim Starten des Streamings sendet der Client die [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) Nachricht.
2.  Beim Streaming fordert der MFT Daten an, indem er ein [metransformneedinput](metransformneedinput.md) -Ereignis sendet. Die Ereignisdaten sind der Datenstrom Bezeichner.
3.  Für jedes [metransformneedinput](metransformneedinput.md) -Ereignis ruft der Client [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) für den angegebenen Stream auf.
4.  Am Ende des Streamings ruft der Client möglicherweise [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) mit der [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) Meldung auf.

Implementierungs Hinweise:

-   Die MFT darf keine [metransformneedinput](metransformneedinput.md) -Ereignisse senden, bis die [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) Nachricht empfangen wird.
-   Während des Streamings sendet der MFT möglicherweise jederzeit [metransformneedinput](metransformneedinput.md) -Ereignisse.
-   Der MFT sollte die Anzahl der ausstehenden [metransformneedinput](metransformneedinput.md) -Ereignisse beibehalten. Alle Aufrufe von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) , die keinem metransformneedinput-Ereignis entsprechen, müssen **MF_E_NOTACCEPTING** zurückgeben.
-   Wenn die MFT die [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) Nachricht empfängt, setzt Sie die Anzahl der ausstehenden [metransformneedinput](metransformneedinput.md) -Ereignisse auf NULL zurück.
-   Der MFT darf keine [metransformneedinput](metransformneedinput.md) -Ereignisse senden, nachdem er die [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) Nachricht empfangen hat.
-   Wenn [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) vor [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) oder nach [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md)aufgerufen wird, muss die Methode **MF_E_NOTACCEPTING** zurückgeben.

## <a name="processoutput"></a>ProcessOutput

Die [**IMF Transform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode wird wie folgt geändert:

1.  Wenn die MFT eine Ausgabe hat, sendet Sie ein [metransformhaveoutput](metransformhaveoutput.md) -Ereignis.
2.  Für jedes [metransformhaveoutput](metransformhaveoutput.md) -Ereignis ruft der Client [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)auf.

Implementierungs Hinweise:

-   Wenn der Client [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) zu einem beliebigen Zeitpunkt aufruft, gibt die Methode **E_UNEXPECTED** zurück.
-   Ein asynchroner MFT sollte niemals **MF_E_TRANSFORM_NEED_MORE_INPUT** von der [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode zurückgeben. Wenn die MFT mehr Eingaben erfordert, sendet Sie ein [metransformneedinput](metransformneedinput.md) -Ereignis.

## <a name="draining"></a>Ernde

Das Entleeren eines MFT bewirkt, dass der MFT so viele Ausgaben erzeugt, wie er von den bereits gesendeten Eingabedaten möglich ist. Das Ableiten einer asynchronen MFT funktioniert wie folgt:

1.  Der Client sendet die [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) Nachricht.
2.  Der MFT sendet weiterhin [metransformhaveoutput](metransformhaveoutput.md) -Ereignisse, bis keine weiteren Daten mehr verarbeitet werden müssen. Während dieser Zeit werden keine [metransformneedinput](metransformneedinput.md) -Ereignisse gesendet.
3.  Nachdem das MFT das letzte [metransformhaveoutput](metransformhaveoutput.md) -Ereignis gesendet hat, sendet es ein [metransformdraunvollständiges](metransformdraincomplete.md) Ereignis.

Nachdem die ENTF-Datei vollständig ist, sendet der MFT kein anderes [metransformneedinput](metransformneedinput.md) -Ereignis, bis eine [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) Meldung vom Client empfangen wird.

## <a name="flushing"></a>Lak

Der Client kann die MFT leeren, indem er die [**MFT_MESSAGE_COMMAND_FLUSH**](mft-message-command-flush.md) Nachricht sendet. Die MFT löscht alle Eingabe-und Ausgabe Beispiele, die Sie enthält.

Der MFT sendet kein anderes [metransformneedinput](metransformneedinput.md) -Ereignis, bis eine [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) Meldung vom Client empfangen wird.

## <a name="markers"></a>Marker

Der Client kann einen Punkt im Stream markieren, indem er die [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) Nachricht sendet. Die MFT antwortet wie folgt:

1.  Der MFT generiert so viele Ausgabe Beispiele wie aus den vorhandenen Eingabedaten und sendet ein [metransformhaveoutput](metransformhaveoutput.md) -Ereignis für jedes Ausgabe Beispiel.
2.  Nachdem die gesamte Ausgabe generiert wurde, sendet der MFT ein [metransformmarker](metransformmarker.md) -Ereignis. Dieses Ereignis muss nach allen [metransformhaveoutput](metransformhaveoutput.md) -Ereignissen gesendet werden.

Nehmen wir beispielsweise an, dass ein Decoder über genügend Eingabedaten verfügt, um vier Ausgabe Beispiele zu liefern. Wenn der Client die [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) Nachricht sendet, werden von der MFT vier [metransformhaveoutput](metransformhaveoutput.md) -Ereignisse (eine pro Ausgabe Stichprobe), gefolgt von einem [metransformmarker](metransformmarker.md) -Ereignis in die Warteschlange eingereiht.

Die markernachricht ähnelt der Ablass Nachricht. Eine Ableitung wird jedoch als Unterbrechung im Stream betrachtet, während ein Marker nicht ist. Das Ableiten von und Markierungen hat die folgenden Unterschiede.

Ernde

-   Während der Ableitung sendet der MFT keine [metransformneedinput](metransformneedinput.md) -Ereignisse.
-   Der MFT verwirft alle Eingabedaten, die nicht zum Erstellen eines Ausgabe Beispiels verwendet werden können.
-   Einige MFTs verursachen am Ende der Daten ein "Fragment". Beispielsweise erzeugen Audioeffekte wie z. b. "Reverb" oder "Echo" zusätzliche Daten, nachdem die Eingabedaten beendet wurden. Ein MFT, das ein Ende generiert, sollte dies am Ende eines Ausgleichs Vorgangs bewirken.
-   Nachdem der MFT-Vorgang abgeschlossen wurde, wird das nächste Ausgabe Beispiel mit dem [**MFSampleExtension_Discontinuity**](mfsampleextension-discontinuity-attribute.md) -Attribut markiert, um eine Diskontinuität im Datenstrom anzugeben.

Setzen

-   Der MFT sendet weiterhin [metransformneedinput](metransformneedinput.md) -Ereignisse vor dem Senden des markerereignisses.
-   Der MFT löscht keine Eingabedaten. Wenn partielle Daten vorhanden sind, sollten Sie nach dem Markerpunkt verarbeitet werden.
-   Der MFT erzeugt am Markerpunkt kein Ende.
-   Das Flag für die Diskontinuität nach dem Markerpunkt wird vom MFT nicht festgelegt.

## <a name="format-changes"></a>Formatieren von Änderungen

Ein asynchroner MFT muss dynamische Formatänderungen unterstützen, wie unter [Verarbeiten von streamänderungen](handling-stream-changes.md)beschrieben.

## <a name="attributes"></a>Attribute

Ein asynchroner MFT muss die [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode implementieren, um einen gültigen Attribut Speicher zurückzugeben. Die folgenden Attribute gelten für asynchrone MFTs:



| Attribut                                                                                    | BESCHREIBUNG                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MF_TRANSFORM_ASYNC](mf-transform-async.md)                                               | Das MFT muss dieses Attribut auf " **true** " festlegen (1). Der Client kann dieses Attribut Abfragen, um zu ermitteln, ob der MFT asynchron ist. |
| [MF_TRANSFORM_ASYNC_UNLOCK](mf-transform-async-unlock.md)                                |                                                                                                                                   |
| [**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**](mft-support-dynamic-format-change-attribute.md) | Das MFT muss dieses Attribut auf " **true** " festlegen (1). Der Client kann davon ausgehen, dass dieses Attribut festgelegt ist.                                |



 

## <a name="unlocking-asynchronous-mfts"></a>Entsperren von asynchronen MFTs

Asynchrone MFTs sind nicht kompatibel mit dem ursprünglichen MFT-Datenverarbeitungs Modell. Um zu verhindern, dass asynchrone MFTs vorhandene Anwendungen unterbrechen, wird der folgende Mechanismus definiert:

<dl> Der Client ruft <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">imftransform:: GetAttributes</a> auf der MFT auf.  
Der Client fragt den für dieses <a href="mf-transform-async.md">MF_TRANSFORM_ASYNC</a> Attribut ab. Für eine asynchrone MFT ist der Wert dieses Attributs " **true**".  
Zum Entsperren des MFT muss der Client das <a href="mf-transform-async-unlock.md">MF_TRANSFORM_ASYNC_UNLOCK</a> -Attribut auf " **true**" festlegen.  
</dl>

Bis der Client die Sperrung des MFT entsperrt, sollten alle [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Methoden **MF_E_TRANSFORM_ASYNC_LOCKED** zurückgeben, mit den folgenden Ausnahmen:

-   [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (alle asynchronen MFTs)
-   [**Imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (alle asynchronen MFTs)
-   [**IMF Transform:: getoutputcurrenttype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (nur Encoder)
-   [**IMF Transform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (nur Encoder)
-   [**IMF Transform:: getstreamcount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (alle asynchronen MFTs)
-   [**IMF Transform:: getstreamids**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (alle asynchronen MFTs)

Der folgende Code zeigt, wie Sie eine asynchrone MFT entsperren:


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="shutting-down-the-mft"></a>Der MFT wird heruntergefahren.

Asynchrone MFTs müssen die [**IMF Shutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) -Schnittstelle implementieren.

-   [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown): die Ereignis Warteschlange muss vom MFT heruntergefahren werden. Wenn Sie die Standard Ereignis Warteschlange verwenden, nennen Sie [**imfmediaeventqueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown). Optional kann der MFT andere Ressourcen freigeben. Der Client darf den MFT nach dem Aufrufen des **herunter** Fahrens nicht verwenden.
-   [**Getshutdownstatus**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus): Nachdem das [**herunter**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown) fahren aufgerufen wurde, sollte der MFT den Wert **MFSHUTDOWN_COMPLETED** im *pstatus* -Parameter zurückgeben. Der Wert **MFSHUTDOWN_INITIATED** sollte nicht zurückgegeben werden.

## <a name="registration-and-enumeration"></a>Registrierung und Enumeration

Um eine asynchrone MFT zu registrieren, müssen Sie die Funktion [**mftregister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) aufrufen und das **MFT_ENUM_FLAG_ASYNCMFT** -Flag im *Flags* -Parameter festlegen. (Zuvor war dieses Flag reserviert.)

Um asynchrone MFTs aufzulisten, müssen Sie die Funktion [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) aufrufen und das **MFT_ENUM_FLAG_ASYNCMFT** -Flag im *Flags* -Parameter festlegen. Aus Gründen der Abwärtskompatibilität listet die [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion keine asynchronen MFTs auf. Andernfalls könnte das Installieren einer asynchronen MFT auf dem Computer des Benutzers vorhandene Anwendungen unterbrechen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 



