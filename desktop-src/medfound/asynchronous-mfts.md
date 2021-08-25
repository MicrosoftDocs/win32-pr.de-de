---
description: In diesem Thema wird die asynchrone Datenverarbeitung für Media Foundation Transformationen (MFTs) beschrieben.
ms.assetid: d438ffae-fc50-454f-8ce4-2d6676500fff
title: Asynchrone MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cab2ef683ef22fd22a911c045a1a744f1c0d561b3e8e66d46ca2cf6c6f0ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959520"
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
-   [Ausgleichen](#draining)
-   [Spülung](#flushing)
-   [Marker](#markers)
-   [Formatänderungen](#format-changes)
-   [Attribute](#attributes)
-   [Entsperren asynchroner MFTs](#unlocking-asynchronous-mfts)
-   [Herunterfahren des MFT](#shutting-down-the-mft)
-   [Registrierung und Enumeration](#registration-and-enumeration)
-   [Zugehörige Themen](#related-topics)

## <a name="about-asynchronous-mfts"></a>Informationen zu asynchronen MFTs

Als MFTs in Windows Vista eingeführt wurden, wurde die API für die *synchrone Datenverarbeitung* entwickelt. In diesem Modell wartet MFT immer entweder darauf, Eingaben zu erhalten oder eine Ausgabe zu erzeugen.

Betrachten Sie einen typischen Videodecoder. Um einen decodierten Frame zu erhalten, ruft der Client [**DEN CLIENT AUF, um DIETransform::P rocessOutput zu erhalten.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) Wenn der Decoder über genügend Daten zum Decodieren eines Frames verfügt, wird **ProcessOutput** blockiert, während der MFT den Frame decodiert. **Andernfalls gibt ProcessOutput** **MF_E_TRANSFORM_NEED_MORE_INPUT** zurück, was angibt, dass der Client [**EINETRANSFORM::P rocessInput aufrufen soll.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)

Dieses Modell funktioniert gut, wenn der Decoder alle seine Decodierungsvorgänge für einen Thread ausführt. Angenommen, der Decoder verwendet mehrere Threads, um Frames parallel zu decodieren. Um die beste Leistung zu erzielen, sollte der Decoder immer dann neue Eingaben empfangen, wenn ein Decodierungsthread in den Leerlauf über geht. Die Rate, mit der Threads Decodierungsvorgänge abschließen, entspricht jedoch nicht genau den Clientaufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) und [**ProcessOutput,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)was dazu führt, dass Threads auf Arbeit warten.

Windows 7 führt eine ereignisgesteuerte,  asynchrone Verarbeitung für MFTs ein. In diesem Modell sendet der MFT immer dann ein Ereignis an den Client, wenn er Eingaben benötigt oder über eine Ausgabe verfügt.

## <a name="general-requirements"></a>Allgemeine Anforderungen

In diesem Thema wird beschrieben, wie sich asynchrone MFTs von synchronem MFT unterscheiden. Sofern in diesem Thema nicht erwähnt, sind die beiden Verarbeitungsmodelle identisch. (Insbesondere ist die Formataushandlung identisch.)

Ein asynchrones MFT muss die folgenden Schnittstellen implementieren:

-   [**VORRÜBERSETZUNGTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**VERERBUNGMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**BEShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

## <a name="events"></a>Ereignisse

Ein asynchroner MFT verwendet die folgenden Ereignisse, um seinen Datenverarbeitungsstatus zu signalisieren:



| Ereignis                                                    | Beschreibung                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [METransformNeedInput](metransformneedinput.md)         | Wird gesendet, wenn MFT mehr Eingaben akzeptieren kann.                          |
| [METransformHaveOutput](metransformhaveoutput.md)       | Wird gesendet, wenn die MFT-Ausgabe auft.                                     |
| [METransformDgreifComplete](metransformdraincomplete.md) | Wird gesendet, wenn ein Entleerungsvorgang abgeschlossen ist. Weitere Informationen [finden Sie unter Leeren von](#draining). |
| [METransformMarker](metransformmarker.md)               | Wird gesendet, wenn ein Marker prozessweise ist. Weitere Informationen [finden Sie unter Marker.](#markers)           |



 

Diese Ereignisse werden out-of-band gesendet. Es ist wichtig, den Unterschied zwischen In-Band- und Out-of-Band-Ereignissen im Kontext eines MFT zu verstehen.

Der ursprüngliche MFT-Entwurf unterstützt *In-Band-Ereignisse.* Ein In-Band-Ereignis enthält Informationen zum Datenstrom, z. B. Informationen zu einer Formatänderung. Der Client sendet In-Band-Ereignisse an MFT, indem er DURCH AUFRUFEN [**von DURCHSICHTTransform::P rocessEvent aufruft.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) Der MFT kann In-Band-Ereignisse in der [**ProcessOutput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) zurück an den Client senden. (Insbesondere werden Ereignisse im **pEvents-Member** [](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer) der MFT_OUTPUT_DATA_BUFFER übermittelt.)

Ein MFT sendet Out-of-Band-Ereignisse wie folgt über die [**BERMEDIAEventGenerator-Schnittstelle:**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)

1.  Der MFT implementiert die [**BERMEDIAEventGenerator-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) wie unter [Media Event Generators (Medienereignis-Generatoren) beschrieben.](media-event-generators.md)
2.  Der Client ruft **IUnknown::QueryInterface** auf der MFT für die [**BENUTZEROBERFLÄCHENmediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) auf. Eine asynchrone MFT muss diese Schnittstelle verfügbar machen. Synchrone MFTs sollten diese Schnittstelle nicht verfügbar machen.
3.  Der Client ruft [**DIE FOLGENDEN Aufrufe auf: 10002222221111111111111111111111111111111111111111111111111111111DMediaEventGenerator::EndGetEvent,um**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) Out-of-Band-Ereignisse von MFT zu empfangen. [](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent)

## <a name="processinput"></a>ProcessInput

Die [**METHODE VERFORMTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) wird wie folgt geändert:

1.  Beim Starten des Streamings sendet der Client [**die**](mft-message-notify-start-of-stream.md) MFT_MESSAGE_NOTIFY_START_OF_STREAM Nachricht.
2.  Während des Streamings fordert der MFT Daten an, indem er ein [METransformNeedInput-Ereignis](metransformneedinput.md) sendet. Die Ereignisdaten sind der Streambezeichner.
3.  Für jedes [METransformNeedInput-Ereignis](metransformneedinput.md) ruft der Client [**ProcessInput für**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) den angegebenen Stream auf.
4.  Am Ende des Streamings kann der Client [**ProcessMessage mit**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) der MFT_MESSAGE_NOTIFY_END_OF_STREAM [**aufrufen.**](mft-message-notify-end-of-stream.md)

Implementierungshinweise:

-   Der MFT darf keine [METransformNeedInput-Ereignisse](metransformneedinput.md) senden, bis er die [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) empfängt.
-   Während des Streamings kann MFT [jederzeit METransformNeedInput-Ereignisse](metransformneedinput.md) senden.
-   MFT sollte die Anzahl ausstehender [METransformNeedInput-Ereignisse](metransformneedinput.md) verwalten. Jeder Aufruf von [**ProcessInput,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) der keinem METransformNeedInput-Ereignis entspricht, **muss** MF_E_NOTACCEPTING.
-   Wenn der MFT die [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) empfängt, wird die Anzahl ausstehender [METransformNeedInput-Ereignisse](metransformneedinput.md) auf 0 (null) zurückgesetzt.
-   Der MFT darf keine [METransformNeedInput-Ereignisse](metransformneedinput.md) senden, nachdem er die MFT_MESSAGE_NOTIFY_END_OF_STREAM [**empfangen**](mft-message-notify-end-of-stream.md) hat.
-   Wenn [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) vor [](mft-message-notify-start-of-stream.md) MFT_MESSAGE_NOTIFY_START_OF_STREAM oder nach MFT_MESSAGE_NOTIFY_END_OF_STREAM aufgerufen [**wird,**](mft-message-notify-end-of-stream.md)muss die Methode **MF_E_NOTACCEPTING.**

## <a name="processoutput"></a>ProcessOutput

Die [**METHODE VERFORMTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) wird wie folgt geändert:

1.  Wenn der MFT eine Ausgabe hat, sendet er ein [METransformHaveOutput-Ereignis.](metransformhaveoutput.md)
2.  Für jedes [METransformHaveOutput-Ereignis](metransformhaveoutput.md) ruft der Client [**ProcessOutput auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)

Implementierungshinweise:

-   Wenn der Client [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) zu einem anderen Zeitpunkt aufruft, gibt die Methode **E_UNEXPECTED.**
-   Ein asynchroner MFT sollte niemals **MF_E_TRANSFORM_NEED_MORE_INPUT** [**ProcessOutput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) zurückgeben. Wenn der MFT mehr Eingaben erfordert, sendet er ein [METransformNeedInput-Ereignis.](metransformneedinput.md)

## <a name="draining"></a>Ausgleichen

Das Entleeren eines MFT führt dazu, dass MFT so viele Ausgaben erzeugt, wie es aus den bereits gesendeten Eingabedaten möglich ist. Das Leeren eines asynchronen MFT funktioniert wie folgt:

1.  Der Client sendet die [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) Nachricht.
2.  Der MFT sendet weiterhin [METransformHaveOutput-Ereignisse,](metransformhaveoutput.md) bis keine Daten mehr zu verarbeiten sind. Während dieser Zeit werden [keine METransformNeedInput-Ereignisse](metransformneedinput.md) gesendet.
3.  Nachdem der MFT das letzte [METransformHaveOutput-Ereignis](metransformhaveoutput.md) sendet, sendet er ein [METransformDgreifComplete-Ereignis.](metransformdraincomplete.md)

Nach Abschluss des Leerens sendet MFT erst dann ein weiteres [METransformNeedInput-Ereignis,](metransformneedinput.md) wenn es eine MFT_MESSAGE_NOTIFY_START_OF_STREAM Clientnachricht empfängt. [](mft-message-notify-start-of-stream.md)

## <a name="flushing"></a>Spülung

Der Client kann den MFT leeren, indem er [**die**](mft-message-command-flush.md) MFT_MESSAGE_COMMAND_FLUSH sendet. Der MFT löscht alle Eingabe- und Ausgabebeispiele, die er hält.

Der MFT sendet erst dann ein weiteres [METransformNeedInput-Ereignis,](metransformneedinput.md) wenn er eine [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) Nachricht vom Client empfängt.

## <a name="markers"></a>Marker

Der Client kann einen Punkt im Stream markieren, indem er die [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) Nachricht sendet. Der MFT antwortet wie folgt:

1.  Der MFT generiert beliebig viele Ausgabebeispiele aus den vorhandenen Eingabedaten und sendet ein [METransformHaveOutput-Ereignis](metransformhaveoutput.md) für jedes Ausgabebeispiel.
2.  Nachdem die gesamte Ausgabe generiert wurde, sendet der MFT ein [METransformMarker-Ereignis.](metransformmarker.md) Dieses Ereignis muss nach allen [METransformHaveOutput-Ereignissen](metransformhaveoutput.md) gesendet werden.

Angenommen, ein Decoder verfügt über genügend Eingabedaten, um vier Ausgabebeispiele zu erzeugen. Wenn der Client die [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) Nachricht sendet, stellt der MFT vier [METransformHaveOutput-Ereignisse](metransformhaveoutput.md) in die Warteschlange (eins pro Ausgabebeispiel), gefolgt von einem [METransformMarker-Ereignis.](metransformmarker.md)

Die Markermeldung ähnelt der Entleerungsmeldung. Eine Entleerung wird jedoch als Unterbrechung im Datenstrom betrachtet, wohingegen ein Marker nicht ist. Die Entleerungen und Marker weisen die folgenden Unterschiede auf.

Entwässerung:

-   Beim Entladen sendet der MFT keine [METransformNeedInput-Ereignisse.](metransformneedinput.md)
-   Der MFT verwirft alle Eingabedaten, die nicht zum Erstellen eines Ausgabebeispiels verwendet werden können.
-   Einige MFTs erzeugen ein "Ende" am Ende der Daten. Beispielsweise erzeugen Audioeffekte wie Hall oder Echo zusätzliche Daten, nachdem die Eingabedaten beendet wurden. Ein MFT, der ein Ende generiert, sollte dies am Ende eines Entleerungsvorgangs tun.
-   Nachdem die MFT-Entleerung abgeschlossen ist, markiert sie das nächste Ausgabebeispiel mit dem [**MFSampleExtension_Discontinuity**](mfsampleextension-discontinuity-attribute.md) Attribut, um eine Diskontinuität im Stream anzugeben.

Marker:

-   Der MFT sendet weiterhin [METransformNeedInput-Ereignisse,](metransformneedinput.md) bevor das Markerereignis gesendet wird.
-   Der MFT verwirft keine Eingabedaten. Wenn Teildaten vorhanden sind, sollten sie nach dem Markerpunkt verarbeitet werden.
-   Der MFT erzeugt am Markerpunkt kein Ende.
-   Der MFT legt das Diskontinuitätsflag nach dem Markerpunkt nicht fest.

## <a name="format-changes"></a>Formatänderungen

Ein asynchroner MFT muss dynamische Formatänderungen unterstützen, wie unter [Verarbeiten von Streamänderungen](handling-stream-changes.md)beschrieben.

## <a name="attributes"></a>Attribute

Ein asynchroner MFT-Wert muss die [**METHODE VONTRANSFORM::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) implementieren, um einen gültigen Attributspeicher zurückzugeben. Die folgenden Attribute gelten für asynchrone MFTs:



| attribute                                                                                    | Beschreibung                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MF_TRANSFORM_ASYNC](mf-transform-async.md)                                               | Der MFT muss dieses Attribut auf **TRUE** (1) festlegen. Der Client kann dieses Attribut abfragen, um zu ermitteln, ob der MFT asynchron ist. |
| [MF_TRANSFORM_ASYNC_UNLOCK](mf-transform-async-unlock.md)                                |                                                                                                                                   |
| [**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**](mft-support-dynamic-format-change-attribute.md) | Der MFT muss dieses Attribut auf **TRUE** (1) festlegen. Der Client kann davon ausgehen, dass dieses Attribut festgelegt ist.                                |



 

## <a name="unlocking-asynchronous-mfts"></a>Entsperren asynchroner MFTs

Asynchrone MFTs sind nicht mit dem ursprünglichen MFT-Datenverarbeitungsmodell kompatibel. Um zu verhindern, dass asynchrone MFTs vorhandene Anwendungen abbrechen, wird der folgende Mechanismus definiert:

<dl> Der Client ruft <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">ÜBERTRANSFORM::GetAttributes</a> für den MFT auf.  
Der Client fragt die nach diesem <a href="mf-transform-async.md">MF_TRANSFORM_ASYNC</a> Attribut ab. Bei einem asynchronen MFT ist der Wert dieses Attributs **TRUE.**  
Um den MFT zu entsperren, muss der Client das <a href="mf-transform-async-unlock.md">MF_TRANSFORM_ASYNC_UNLOCK-Attribut</a> auf **TRUE** setzen.  
</dl>

Bis der Client den MFT entsperrt, sollten alle [**METHODEN VONTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) mit den folgenden Ausnahmen **MF_E_TRANSFORM_ASYNC_LOCKED** zurückgeben:

-   [**SUBSCRIBERTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (alle asynchronen MFTs)
-   [**SUBSCRIBERTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (alle asynchronen MFTs)
-   [**CODTRANSFORM::GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (nur Encoder)
-   [**CODTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (nur Encoder)
-   [**SUBSCRIBERTransform::GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (alle asynchronen MFTs)
-   [**SUBSCRIBERTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (alle asynchronen MFTs)

Der folgende Code zeigt, wie Ein asynchroner MFT entsperrt wird:


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



## <a name="shutting-down-the-mft"></a>Herunterfahren des MFT

Asynchrone MFTs müssen die [**INTERFACESShutdown-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) implementieren.

-   [**Herunterfahren:**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown)Der MFT muss seine Ereigniswarteschlange herunterfahren. Wenn Sie die Standardereigniswarteschlange verwenden, rufen Sie [**DENMEDIAEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown)auf. Optional kann der MFT andere Ressourcen freigeben. Der Client darf den MFT nach dem Aufruf von **Shutdown** nicht mehr verwenden.
-   [**GetShutdownStatus:**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus)Nachdem [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown) aufgerufen wurde, sollte der MFT den Wert **MFSHUTDOWN_COMPLETED** im *pStatus-Parameter* zurückgeben. Der Wert **MFSHUTDOWN_INITIATED** sollte nicht zurückgegeben werden.

## <a name="registration-and-enumeration"></a>Registrierung und Enumeration

Um einen asynchronen MFT zu registrieren, rufen Sie die [**MFTRegister-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) auf, und legen Sie das **flag MFT_ENUM_FLAG_ASYNCMFT** im *Flags-Parameter* fest. (Zuvor war dieses Flag reserviert.)

Um asynchrone MFTs aufzuzählen, rufen Sie die [**MFTEnumEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) auf, und legen Sie das **flag MFT_ENUM_FLAG_ASYNCMFT** im *Flags-Parameter* fest. Aus Gründen der Abwärtskompatibilität führt die [**MFTEnum-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) keine asynchronen MFTs auf. Andernfalls kann die Installation eines asynchronen MFT auf dem Computer des Benutzers vorhandene Anwendungen unterbrechen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> </dl>

 

 



