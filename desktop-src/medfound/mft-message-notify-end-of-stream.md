---
description: Benachrichtigt eine Media Foundation Transformation (MFT), dass ein Eingabestream beendet wurde.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476781b149553bec1d48632e0621ff0a38ad8d21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360004"
---
# <a name="mft_message_notify_end_of_stream"></a>\_ \_ \_ Ende \_ des Daten \_ Stroms für MFT-Nachricht Benachrichtigen

Benachrichtigt eine Media Foundation Transformation (MFT), dass ein Eingabestream beendet wurde.

## <a name="message-parameter"></a>Message-Parameter

Der *ulparam* -Parameter enthält den Bezeichner des Eingabedaten Stroms, der als **DWORD** -Wert angegeben wird. Platzieren Sie diesen Wert in 64-Bit-Anwendungen in den unteren 32-Bits des **ulong \_ ptr**.

## <a name="remarks"></a>Bemerkungen

Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Der Client muss diese Nachricht nicht senden.

Nachdem ein Stream beendet wurde, kann der Client erneut [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) aufrufen, um neue Daten für diesen Stream zu senden. Wenn dies der Fall ist, muss der Client das Diskontinuität-Attribut ([**mfsampleextension \_ Diskontinuität**](mfsampleextension-discontinuity-attribute.md) -Attribut) für das erste Eingabe Beispiel festlegen, nachdem der Stream beendet wurde. (Der Client sollte dieses Attribut immer auf dem ersten neuen Beispiel festlegen, nachdem ein Stream beendet wurde, unabhängig davon, ob der Client die Nachricht zum **\_ \_ \_ Ende \_ der \_ Nachricht zum Nachrichten Ende der MFT-Nachricht** gesendet hat. Weitere Informationen zur Behandlung von Diskontinuitäten finden Sie unter [Grundlegendes MFT-Verarbeitungsmodell](basic-mft-processing-model.md).)

Nachdem diese Nachricht für jeden Eingabestream gesendet wurde, sendet der Client in der Regel einen Befehl zum **leeren der MFT- \_ Nachrichten \_ Befehle \_** und sammelt dann die verbleibende Ausgabe. Der Client muss die MFT jedoch nicht entladen. Wenn der Client die MFT nicht abschließt, werden vom MFT in der Regel alle nicht verarbeiteten Daten beim nächsten Aufrufen von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)verworfen, wenn die Datenstrom Diskontinuität erkannt wird. Alternativ kann der Client die MFT leeren, bevor **ProcessInput** aufgerufen wird.

Diese Meldung entfernt den Eingabestream nicht oder setzt den Medientyp zurück.

### <a name="implementation"></a>Implementierung

Ein MFT ist nicht erforderlich, um auf diese Nachricht zu reagieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MFT \_ - \_ Nachrichtentyp**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




