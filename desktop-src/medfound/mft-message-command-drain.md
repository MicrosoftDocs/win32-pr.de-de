---
description: 'MFT_MESSAGE_COMMAND_DRAIN: Fordert eine Media Foundation-Transformation (MFT) an, um alle gespeicherten Daten zu leeren.'
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907bfbd888b1eccbe7336c0d8f386d3266fd8e9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092748"
---
# <a name="mft_message_command_drain"></a>MFT \_ MESSAGE \_ COMMAND \_ DRAIN

Fordert eine Media Foundation-Transformation (MFT) an, um alle gespeicherten Daten zu leeren.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Bemerkungen

Um diese Nachricht zu senden, rufen Sie [**ÜBERTRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

Nachdem diese Nachricht gesendet wurde, akzeptiert der angegebene Eingabestream keine Eingaben, bis der MFT alle Daten aus vorherigen Aufrufen von [**ÜBERTRANSFORM::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)verarbeitet.

Der Ausgleichsprozess variiert geringfügig zwischen synchronen und asynchronen MFTs:

**Synchrone MFTs**

1.  Nachdem der Client diese Nachricht gesendet hat, ruft er [**ÜBERTRANSFORM::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in einer Schleife auf, bis **ProcessOutput** den Fehlercode **MF E TRANSFORM NEED MORE \_ \_ \_ \_ \_ INPUT** zurückgibt.
2.  Solange der MFT noch über zu verarbeitende Daten verfügt, schlagen weitere Aufrufe von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) fehl. Der MFT erzeugt weiterhin Eine Ausgabe, bis alle gespeicherten Daten verwendet werden. Der MFT verwirft alle Daten, die nicht in einem vollständigen Ausgabebeispiel verarbeitet werden können. (Es sollte z. B. ein Teilvideorahmen fallen.)

**Asynchrone MFTs**

1.  Der MFT sendet weiterhin [METransformHaveOutput-Ereignisse,](metransformhaveoutput.md) bis keine daten mehr verarbeitet werden müssen. Während dieser Zeit werden keine [METransformNeedInput-Ereignisse](metransformneedinput.md) gesendet.
2.  Nachdem der MFT das letzte [METransformHaveOutput-Ereignis](metransformhaveoutput.md) gesendet hat, sendet er ein [METransformDrainComplete-Ereignis.](metransformdraincomplete.md)
3.  Nach Abschluss der Entleerung sendet der MFT erst dann ein weiteres [METransformNeedInput-Ereignis,](metransformneedinput.md) wenn er eine [**MFT \_ MESSAGE NOTIFY START OF \_ \_ \_ \_ STREAM-Nachricht**](mft-message-notify-start-of-stream.md) vom Client empfängt.

Nachdem der Client den MFT entladen hat, kann der Client weitere Eingabedaten senden. Das erste Beispiel nach dem Entleerungsvorgang muss über das Diskontinuitätsattribut ([**MFSampleExtension \_ Discontinuity-Attribut)**](mfsampleextension-discontinuity-attribute.md) verfügen.

> [!Note]  
> In früheren Versionen dieser Dokumentation wurde angegeben, dass *der ulParam-Ereignisparameter* ein Member der [**\_ MFT \_ DRAIN \_ TYPE-Enumeration**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) ist. Diese Antwort ist falsch. *UlParam enthält* einen Streambezeichner.

 

### <a name="implementation"></a>Implementierung

Ein asynchrones MFT muss nach dem [Entleeren immer METransformDgreifComplete](metransformdraincomplete.md) zurückgeben.

Ein synchroner MFT kann diese Meldung ignorieren und S \_ OK zurückgeben, wenn die folgenden Bedingungen erfüllt sind:

-   MFT speichert nie mehr als ein Eingabebeispiel gleichzeitig.
-   Jedes Eingabebeispiel erzeugt ein einzelnes Ausgabebeispiel.

Andernfalls muss eine synchrone MFT diese Meldung implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_MFT-NACHRICHTENTYP \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> </dl>

 

 




