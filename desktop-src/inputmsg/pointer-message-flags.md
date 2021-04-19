---
title: Zeigernachrichtenflags
description: Werte, die in verschiedenen Zeiger Makros verwendet werden (siehe Makros).
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
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346736"
---
# <a name="pointer-message-flags"></a>Zeigernachrichtenflags

Werte, die in verschiedenen Zeiger Makros verwendet werden (siehe [Makros](macros.md)).

<dl> <dt>

<span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Gibt den Eingang eines neuen Zeigers an.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Gibt an, dass dieser Zeiger weiterhin vorhanden ist. Wenn dieses Flag nicht festgelegt ist, gibt es an, dass der Zeiger den linken Erkennungsbereich aufweist.

Dieses Flag wird in der Regel nicht festgelegt, wenn ein Mauszeiger den Erkennungsbereich verlässt (**POINTER_FLAG_UPDATE** festgelegt ist) oder wenn ein Zeiger im Kontakt mit einer Fenster Oberfläche den Erkennungsbereich verlässt (**POINTER_FLAG_UP** ist festgelegt).


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Gibt an, dass sich dieser Zeiger in Verbindung mit der Digitalisierungs Oberfläche befindet. Wenn dieses Flag nicht festgelegt ist, gibt es einen Mauszeiger an.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Gibt eine primäre Aktion an, analog zu einer linken Maustaste.

Für einen Fingerabdruck wird dieses Flag festgelegt, wenn es sich im Kontakt mit der Digitalisierungs Oberfläche befindet.

Bei einem Stift Zeiger wird dieses Flag festgelegt, wenn es sich auf der digitalisiereroberfläche befindet und keine Schaltflächen gedrückt sind.

Ein Mauszeiger hat dieses Flag festgelegt, wenn die linke Maustaste gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Gibt eine sekundäre Aktion analog zu einer rechten Maustaste an.

Ein Fingerabdruck verwendet dieses Flag nicht.

Bei einem Stift Zeiger wird dieses Flag festgelegt, wenn es sich im Kontakt mit der Digitalisierungs Oberfläche befindet, auf die die Stift Taste gedrückt wird.

Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die Rechte Maustaste gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Analog zu einem Mausrad-Button.

Ein Fingerabdruck verwendet dieses Flag nicht.

Dieses Flag wird von einem Stift Zeiger nicht verwendet.

Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die Maustaste gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Analog zu einer ersten erweiterten mouseschaltfläche (XButton1).

Ein Fingerabdruck verwendet dieses Flag nicht.

Dieses Flag wird von einem Stift Zeiger nicht verwendet.

Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die erste erweiterte Maus (XButton1) gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Analog zu einer zweiten erweiterten mouseschaltfläche (XButton2).

Ein Fingerabdruck verwendet dieses Flag nicht.

Dieses Flag wird von einem Stift Zeiger nicht verwendet.

Ein Mauszeiger hat dieses Flag festgelegt, wenn die zweite erweiterte Maus (XButton2) gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Gibt an, dass dieser Zeiger als primärer Zeiger festgelegt wurde. Ein primärer Zeiger ist ein einzelner Zeiger, der über diejenigen hinaus Aktionen ausführen kann, die für nicht-primär Zeiger verfügbar sind. Wenn ein primärer Zeiger z. b. einen Kontakt mit einer Fenster-Oberfläche herstellt, kann er das Fenster aktivieren, indem er eine WM_POINTERACTIVATE Nachricht sendet.

Der primäre Zeiger wird von allen aktuellen Benutzerinteraktionen im System (Maus, Toucheingabe, Stift usw.) identifiziert. Daher ist der primäre Zeiger möglicherweise nicht mit Ihrer APP verknüpft. Der erste Kontakt in einer Multitouch-Interaktion ist als primärer Zeiger festgelegt. Wenn ein primärer Zeiger identifiziert wird, müssen alle Kontakte angehoben werden, bevor ein neuer Kontakt als primärer Zeiger identifiziert werden kann. Für apps, die keine Zeiger Eingaben verarbeiten, werden nur die Ereignisse des primären Zeigers zu Mausereignissen herauf gestuft.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Vertrauen ist ein Vorschlag vom Quellgerät, ob der Zeiger eine beabsichtigte oder versehentliche Interaktion darstellt. Dies ist besonders relevant für PT_TOUCH Zeiger, bei denen eine versehentliche Interaktion (z. b. mit der Handtasche) Eingaben auslöst. Das vorhanden sein dieses Flags gibt an, dass das Quellgerät sehr sicher ist, dass diese Eingabe Teil einer beabsichtigten Interaktion ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Gibt an, dass der Zeiger nicht ordnungsgemäß abbricht, z. b. wenn das System ungültige Eingaben für den Zeiger empfängt oder wenn ein Gerät mit aktiven Zeigern abrupt abweicht. Wenn sich die Anwendung, die die Eingabe empfängt, an einer anderen Position befindet, sollte Sie die Interaktion als nicht abgeschlossen behandeln und alle Auswirkungen des betreffenden Zeigers umkehren.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

XButton1 und XButton2 sind zusätzliche Schaltflächen, die auf vielen Maus Geräten verwendet werden. Sie geben dieselben Daten zurück wie Standard-Maustasten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konstanten](constants.md)
</dt> <dt>

[Makros](macros.md)
</dt> </dl>

 

 





