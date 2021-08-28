---
description: 'MFT_MESSAGE_COMMAND_DRAIN: Fordert eine Media Foundation Transformation (MFT) an, um alle gespeicherten Daten zu leeren.'
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8faf20ca1169d87370a7dc1b5a128b11c9f17937a514f4aaea37631aee4d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012620"
---
# <a name="mft_message_command_drain"></a>LEEREN DES \_ MFT-NACHRICHTENBEFEHLS \_ \_

Fordert eine Media Foundation (MFT) an, um alle gespeicherten Daten zu leeren.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Hinweise

Um diese Nachricht zu senden, rufen [**Sie DIETRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

Nachdem diese Nachricht gesendet wurde, akzeptiert der angegebene Eingabestream keine Eingaben, bis der MFT alle Daten aus vorherigen Aufrufen von [**DURCHZEIGTransform::P rocessInput verarbeitet.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)

Der Entleerungsprozess variiert geringfügig zwischen synchronen MFTs und asynchronen MFTs:

**Synchrone MFTs**

1.  Nachdem der Client diese Nachricht gesendet hat, ruft er IN EINER -Schleife [**DEN WERTTRANSFORM::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) auf, bis **ProcessOutput** den Fehlercode **MF \_ E TRANSFORM NEED MORE INPUT \_ \_ \_ \_ zurückgibt.**
2.  Solange der MFT noch Daten zu verarbeiten hat, können weitere Aufrufe von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) nicht mehr möglich sein. MFT erzeugt weiterhin Eine Ausgabe, bis alle gespeicherten Daten verwendet werden. MFT verwirft alle Daten, die nicht in einem vollständigen Ausgabebeispiel verarbeitet werden können. (Es sollte z. B. ein teiler Videoframe ablegen.)

**Asynchrone MFTs**

1.  Der MFT sendet weiterhin [METransformHaveOutput-Ereignisse,](metransformhaveoutput.md) bis keine Daten mehr zu verarbeiten sind. Während dieser Zeit werden [keine METransformNeedInput-Ereignisse](metransformneedinput.md) gesendet.
2.  Nachdem der MFT das letzte [METransformHaveOutput-Ereignis](metransformhaveoutput.md) sendet, sendet er ein [METransformDgreifComplete-Ereignis.](metransformdraincomplete.md)
3.  Nach Abschluss des Leerens sendet MFT erst dann ein weiteres [METransformNeedInput-Ereignis,](metransformneedinput.md) wenn eine [**MFT \_ MESSAGE NOTIFY START OF \_ \_ \_ \_ STREAM-Nachricht**](mft-message-notify-start-of-stream.md) vom Client empfangen wird.

Nachdem der Client die MFT-Daten entleert hat, kann er weitere Eingabedaten senden. Das erste Beispiel nach dem Entleerungsvorgang muss über das Diskontinuitätsattribut ([**MFSampleExtension \_ Discontinuity-Attribut)**](mfsampleextension-discontinuity-attribute.md) verfügen.

> [!Note]  
> In früheren Versionen dieser Dokumentation wurde angegeben, dass *der ulParam-Ereignisparameter* ein Member der [**\_ MFT \_ DRAIN \_ TYPE-Enumeration**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) ist. Diese Antwort ist falsch. *UlParam enthält* einen Streambezeichner.

 

### <a name="implementation"></a>Implementierung

Ein asynchrones MFT muss nach dem [Entleeren immer METransformDgreifComplete](metransformdraincomplete.md) zurückgeben.

Ein synchroner MFT kann diese Meldung ignorieren und S \_ OK zurückgeben, wenn die folgenden Bedingungen erfüllt sind:

-   MFT speichert nie mehr als ein Eingabebeispiel gleichzeitig.
-   Jedes Eingabebeispiel erzeugt ein einzelnes Ausgabebeispiel.

Andernfalls muss eine synchrone MFT diese Meldung implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_MFT-NACHRICHTENTYP \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> </dl>

 

 




