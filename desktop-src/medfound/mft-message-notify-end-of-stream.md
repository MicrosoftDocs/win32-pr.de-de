---
description: Benachrichtigt eine Media Foundation-Transformation (MFT), dass ein Eingabestream beendet wurde.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951337fb91a26f1498b2aa82d42754fb2954ab649b4a021d37d42047be331ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872160"
---
# <a name="mft_message_notify_end_of_stream"></a>MFT \_ MESSAGE \_ NOTIFY \_ END \_ OF \_ STREAM

Benachrichtigt eine Media Foundation-Transformation (MFT), dass ein Eingabestream beendet wurde.

## <a name="message-parameter"></a>Message-Parameter

Der *ulParam-Parameter* enthält den Bezeichner des Eingabestreams, der als **DWORD-Wert** angegeben ist. Platzieren Sie diesen Wert in 64-Bit-Anwendungen in den unteren 32 Bits des **ULONG \_ PTR**.

## <a name="remarks"></a>Hinweise

Um diese Nachricht zu senden, rufen Sie [**ÜBERTRANSFORM::P rocessMessage auf.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)

Der Client muss diese Nachricht nicht senden.

Nach dem Beenden eines Streams kann der Client [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) erneut aufrufen, um neue Daten für diesen Stream zu senden. In diesem Falle muss der Client das Diskontinuitätsattribut [**(MFSampleExtension \_ Discontinuity-Attribut)**](mfsampleextension-discontinuity-attribute.md) für das erste Eingabebeispiel nach dem Ende des Streams festlegen. (Der Client sollte dieses Attribut immer für das erste neue Beispiel festlegen, nachdem ein Stream beendet wurde, unabhängig davon, ob der Client die **MFT \_ MESSAGE NOTIFY END OF \_ \_ \_ \_ STREAM-Nachricht** gesendet hat. Weitere Informationen zur Behandlung von Diskontinuitäten finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell](basic-mft-processing-model.md).)

Nach dem Senden dieser Nachricht für jeden Eingabestream sendet der Client in der Regel einen **MFT \_ MESSAGE COMMAND \_ \_ DRAIN-Befehl** und erfasst dann die verbleibende Ausgabe. Der Client ist jedoch nicht zum Entladen des MFT erforderlich. Wenn der Client den MFT nicht leert, verwirft der MFT in der Regel alle nicht verarbeiteten Daten beim nächsten Aufruf von [**ProcessInput,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)wenn die Diskontinuität des Streams erkannt wird. Alternativ kann der Client den MFT vor dem Aufruf von **ProcessInput** leeren.

Diese Meldung entfernt weder den Eingabestream noch setzt den Medientyp zurück.

### <a name="implementation"></a>Implementierung

Ein MFT ist nicht erforderlich, um auf diese Nachricht zu reagieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_MFT-NACHRICHTENTYP \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




