---
title: Zeigermeldungsflags
description: Werte, die in verschiedenen Zeigermakros verwendet werden (siehe Makros).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 70d329c6a48eb92f6f50ff49d5543c2aaf5cfc3ce9ef23b48290c7aa029eecf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602351"
---
# <a name="pointer-message-flags"></a>Zeigermeldungsflags

Werte, die in verschiedenen Zeigermakros verwendet werden (siehe [Makros](macros.md)).

<dl> <dt>

<span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Gibt die Ankunft eines neuen Zeigers an.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Gibt an, dass dieser Zeiger weiterhin vorhanden ist. Wenn dieses Flag nicht festgelegt ist, gibt es an, dass der Zeiger den linken Erkennungsbereich hat.

Dieses Flag wird in der Regel nicht festgelegt, wenn ein zeigende Zeiger den Erkennungsbereich verlässt (**POINTER_FLAG_UPDATE** ist festgelegt) oder wenn ein Zeiger, der mit einer Fensteroberfläche in Kontakt steht, den Erkennungsbereich verlässt (**POINTER_FLAG_UP** festgelegt ist).


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Gibt an, dass dieser Zeiger mit der Digitizeroberfläche in Kontakt steht. Wenn dieses Flag nicht festgelegt ist, weist es auf einen zeigenden Zeiger hin.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Gibt eine primäre Aktion analog zu einer linken Maustaste nach unten an.

Bei einem Berührungszeiger ist dieses Flag festgelegt, wenn er mit der Digitizeroberfläche in Kontakt ist.

Bei einem Stiftzeiger ist dieses Flag festgelegt, wenn er mit der Digitizeroberfläche in Kontakt ist, ohne dass Schaltflächen gedrückt sind.

Bei einem Mauszeiger ist dieses Flag festgelegt, wenn die linke Maustaste gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Gibt eine sekundäre Aktion analog zu einer rechten Maustaste nach unten an.

Ein Touchzeiger verwendet dieses Flag nicht.

Bei einem Stiftzeiger ist dieses Flag festgelegt, wenn er mit der Digitizeroberfläche in Kontakt ist, während die Stifttaste gedrückt ist.

Bei einem Mauszeiger ist dieses Flag festgelegt, wenn die rechte Maustaste gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Analog zu einer nach unten fahrenden Maustaste.

Ein Touchzeiger verwendet dieses Flag nicht.

Ein Stiftzeiger verwendet dieses Flag nicht.

Bei einem Mauszeiger ist dieses Flag festgelegt, wenn das Mausrad gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Analog zu einer ersten erweiterten Maustaste (XButton1) nach unten.

Ein Touchzeiger verwendet dieses Flag nicht.

Ein Stiftzeiger verwendet dieses Flag nicht.

Bei einem Mauszeiger ist dieses Flag festgelegt, wenn die erste erweiterte Mausschaltfläche (XBUTTON1) aus ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Analog zu einer zweiten erweiterten Mausschaltfläche (XButton2) nach unten.

Ein Touchzeiger verwendet dieses Flag nicht.

Ein Stiftzeiger verwendet dieses Flag nicht.

Bei einem Mauszeiger ist dieses Flag festgelegt, wenn die zweite erweiterte Mausschaltfläche (XBUTTON2) aus ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Gibt an, dass dieser Zeiger als primärer Zeiger festgelegt wurde. Ein primärer Zeiger ist ein einzelner Zeiger, der Aktionen ausführen kann, die über die aktionen hinausgehen, die für nicht primäre Zeiger verfügbar sind. Wenn z. B. ein primärer Zeiger kontaktiert mit der Oberfläche eines Fensters, bietet er dem Fenster möglicherweise die Möglichkeit, sich zu aktivieren, indem er ihm eine WM_POINTERACTIVATE sendet.

Der primäre Zeiger wird aus allen aktuellen Benutzerinteraktionen im System (Maus, Fingerbewegung, Stift und so weiter) identifiziert. Daher ist der primäre Zeiger Ihrer App möglicherweise nicht zugeordnet. Der erste Kontakt in einer Multi-Touch-Interaktion wird als primärer Zeiger festgelegt. Sobald ein primärer Zeiger identifiziert wurde, müssen alle Kontakte aufgehoben werden, bevor ein neuer Kontakt als primärer Zeiger identifiziert werden kann. Bei Apps, die keine Zeigereingabe verarbeiten, werden nur die Ereignisse des primären Zeigers zu Mausereignissen promotet.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Vertrauen ist ein Vorschlag des Quellgeräts darüber, ob der Zeiger eine beabsichtigte oder versehentliche Interaktion darstellt. Dies ist besonders für PT_TOUCH-Zeiger relevant, bei denen eine versehentliche Interaktion (z. B. mit der Handfläche) eine Eingabe auslösen kann. Das Vorhandensein dieses Flags gibt an, dass das Quellgerät sehr sicher ist, dass diese Eingabe Teil einer beabsichtigten Interaktion ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Gibt an, dass der Zeiger nicht normal ist, z. B. wenn das System ungültige Eingaben für den Zeiger empfängt oder wenn ein Gerät mit aktiven Zeigern plötzlich beendet wird. Wenn sich die Anwendung, die die Eingabe empfängt, in der Lage ist, dies zu tun, sollte sie die Interaktion als nicht abgeschlossen behandeln und alle Auswirkungen des betreffenden Zeigers umkehren.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

XBUTTON1 und XBUTTON2 sind zusätzliche Schaltflächen, die auf vielen Mausgeräten verwendet werden. Sie geben die gleichen Daten zurück wie standarde Maustasten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konstanten](constants.md)
</dt> <dt>

[Makros](macros.md)
</dt> </dl>

 

 





