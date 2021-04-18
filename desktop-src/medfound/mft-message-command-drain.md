---
description: Fordert eine Media Foundation Transformation (MFT) an, um alle gespeicherten Daten zu leeren.
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa533cfddfda53fd8eb0ee512b0535aaf9ad8f88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343424"
---
# <a name="mft_message_command_drain"></a>MFT- \_ Nachrichten \_ Befehls \_ Ableitung

Fordert eine Media Foundation Transformation (MFT) an, um alle gespeicherten Daten zu leeren.

## <a name="message-parameter"></a>Message-Parameter

Keine.

## <a name="remarks"></a>Bemerkungen

Um diese Nachricht zu senden, nennen Sie [**imftransform::P rocess Message**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Nachdem diese Nachricht gesendet wurde, akzeptiert der angegebene Eingabedaten Strom erst dann Eingaben, wenn der MFT alle Daten aus vorherigen Aufrufen von [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)verarbeitet hat.

Der Entleerungsprozess variiert geringfügig zwischen synchronen und asynchronen MFTs:

**Synchrone MFTs**

1.  Nachdem der Client diese Nachricht gesendet hat, ruft er [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in einer Schleife auf, bis **ProcessOutput** den Fehlercode **MF-E- \_ \_ Transformation \_ benötigt \_ mehr \_ Eingaben** zurückgibt.
2.  Solange die MFT noch Daten verarbeiten kann, schlagen weitere Aufrufe von [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) fehl. Der MFT erzeugt die Ausgabe so lange, bis alle gespeicherten Daten verwendet werden. Der MFT verwirft alle Daten, die nicht verarbeitet werden können, in ein vollständiges Ausgabe Beispiel. (Sie sollten z. b. einen Teil Videorahmen löschen.)

**Asynchrone MFTs**

1.  Der MFT sendet weiterhin [metransformhaveoutput](metransformhaveoutput.md) -Ereignisse, bis keine weiteren Daten mehr verarbeitet werden müssen. Während dieser Zeit werden keine [metransformneedinput](metransformneedinput.md) -Ereignisse gesendet.
2.  Nachdem das MFT das letzte [metransformhaveoutput](metransformhaveoutput.md) -Ereignis gesendet hat, sendet es ein [metransformdraunvollständiges](metransformdraincomplete.md) Ereignis.
3.  Nachdem das Entpacken vollständig ist, sendet der MFT kein anderes [metransformneedinput](metransformneedinput.md) -Ereignis, bis er eine Nachricht zum [**\_ \_ \_ Starten des Nachrichten Starts \_ von \_ MFT**](mft-message-notify-start-of-stream.md) vom Client empfängt.

Nachdem der Client die MFT entladen hat, kann der Client weitere Eingabedaten senden. Das erste Beispiel nach dem Entladen-Vorgang muss das Diskontinuität-Attribut ([**MF SampleExtension \_ Diskontinuität**](mfsampleextension-discontinuity-attribute.md) -Attribut) aufweisen.

> [!Note]  
> In früheren Versionen dieser Dokumentation wurde angegeben, dass der *ulparam* -Ereignis Parameter ein Member der Enumeration des [**\_ MFT-Ausgleichs \_ \_ Typs**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) ist. Diese Antwort ist falsch. *Ulparam* enthält einen Datenstrom Bezeichner.

 

### <a name="implementation"></a>Implementierung

Ein asynchroner MFT muss immer [metransformdraunvollzurück](metransformdraincomplete.md) geben, nachdem er entladen wurde.

Eine synchrone MFT kann diese Meldung ignorieren und S OK zurückgeben, \_ Wenn die folgenden Bedingungen zutreffen:

-   Der MFT speichert niemals mehr als eine Eingabe Stichprobe.
-   Jedes Eingabe Beispiel erzeugt ein einzelnes Ausgabe Beispiel.

Andernfalls muss eine synchrone MFT diese Meldung implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MFT \_ - \_ Nachrichtentyp**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[Asynchrone MFTs](asynchronous-mfts.md)
</dt> </dl>

 

 




