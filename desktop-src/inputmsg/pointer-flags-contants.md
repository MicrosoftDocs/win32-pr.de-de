---
title: Zeigerflags
description: Werte, die im Feld pointerflags der POINTER_INFO Struktur angezeigt werden können.
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 21a4191aa09bcb0cb9fda1a4c9bc011d978e203a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742329"
---
# <a name="pointer-flags"></a>Zeigerflags

Werte, die im Feld **pointerflags** der [**POINTER_INFO**](/previous-versions/windows/desktop/api) Struktur angezeigt werden können.

<dl> <dt>

<span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Standard


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Gibt den Eingang eines neuen Zeigers an.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Gibt an, dass dieser Zeiger weiterhin vorhanden ist. Wenn dieses Flag nicht festgelegt ist, gibt es an, dass der Zeiger den linken Erkennungsbereich aufweist.

Dieses Flag wird in der Regel nicht festgelegt, wenn ein Mauszeiger den Erkennungsbereich verlässt (**POINTER_FLAG_UPDATE** festgelegt ist) oder wenn ein Zeiger im Kontakt mit einer Fenster Oberfläche den Erkennungsbereich verlässt (**POINTER_FLAG_UP** ist festgelegt).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Gibt an, dass sich dieser Zeiger in Verbindung mit der Digitalisierungs Oberfläche befindet. Wenn dieses Flag nicht festgelegt ist, gibt es einen Mauszeiger an.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Gibt eine primäre Aktion an, analog zu einer linken Maustaste.

Für einen Fingerabdruck wird dieses Flag festgelegt, wenn es sich im Kontakt mit der Digitalisierungs Oberfläche befindet.

Bei einem Stift Zeiger wird dieses Flag festgelegt, wenn es sich auf der digitalisiereroberfläche befindet und keine Schaltflächen gedrückt sind.

Ein Mauszeiger hat dieses Flag festgelegt, wenn die linke Maustaste gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Gibt eine sekundäre Aktion analog zu einer rechten Maustaste an.

Ein Fingerabdruck verwendet dieses Flag nicht.

Bei einem Stift Zeiger wird dieses Flag festgelegt, wenn es sich im Kontakt mit der Digitalisierungs Oberfläche befindet, auf die die Stift Taste gedrückt wird.

Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die Rechte Maustaste gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Analog zu einem Mausrad-Button.

Ein Fingerabdruck verwendet dieses Flag nicht.

Dieses Flag wird von einem Stift Zeiger nicht verwendet.

Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die Maustaste gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Analog zu einer ersten erweiterten mouseschaltfläche (XButton1).

Ein Fingerabdruck verwendet dieses Flag nicht.

Dieses Flag wird von einem Stift Zeiger nicht verwendet.

Bei einem Mauszeiger wird dieses Flag festgelegt, wenn die erste erweiterte Maus (XButton1) gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Analog zu einer zweiten erweiterten mouseschaltfläche (XButton2).

Ein Fingerabdruck verwendet dieses Flag nicht.

Dieses Flag wird von einem Stift Zeiger nicht verwendet.

Ein Mauszeiger hat dieses Flag festgelegt, wenn die zweite erweiterte Maus (XButton2) gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Gibt an, dass dieser Zeiger als primärer Zeiger festgelegt wurde. Ein primärer Zeiger ist ein einzelner Zeiger, der über diejenigen hinaus Aktionen ausführen kann, die für nicht-primär Zeiger verfügbar sind. Wenn ein primärer Zeiger z. b. einen Kontakt mit einer Fenster-Oberfläche herstellt, kann er das Fenster aktivieren, indem er eine [**WM_POINTERACTIVATE**](wm-pointeractivate.md) Nachricht sendet.

Der primäre Zeiger wird von allen aktuellen Benutzerinteraktionen im System (Maus, Toucheingabe, Stift usw.) identifiziert. Daher ist der primäre Zeiger möglicherweise nicht mit Ihrer APP verknüpft. Der erste Kontakt in einer Multitouch-Interaktion ist als primärer Zeiger festgelegt. Wenn ein primärer Zeiger identifiziert wird, müssen alle Kontakte angehoben werden, bevor ein neuer Kontakt als primärer Zeiger identifiziert werden kann. Für apps, die keine Zeiger Eingaben verarbeiten, werden nur die Ereignisse des primären Zeigers zu Mausereignissen herauf gestuft.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x000004000
</dt> <dt>



Vertrauen ist ein Vorschlag vom Quellgerät, ob der Zeiger eine beabsichtigte oder versehentliche Interaktion darstellt. Dies ist besonders relevant für PT_TOUCH Zeiger, bei denen eine versehentliche Interaktion (z. b. mit der Handtasche) Eingaben auslöst. Das vorhanden sein dieses Flags gibt an, dass das Quellgerät sehr sicher ist, dass diese Eingabe Teil einer beabsichtigten Interaktion ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x000008000
</dt> <dt>



Gibt an, dass der Zeiger nicht ordnungsgemäß abbricht, z. b. wenn das System ungültige Eingaben für den Zeiger empfängt oder wenn ein Gerät mit aktiven Zeigern abrupt abweicht. Wenn sich die Anwendung, die die Eingabe empfängt, an einer anderen Position befindet, sollte Sie die Interaktion als nicht abgeschlossen behandeln und alle Auswirkungen des betreffenden Zeigers umkehren.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Gibt an, dass dieser Zeiger in den Zustand "nach unten" übergeht. Das heißt, es wurde eine Verbindung mit der digitalisiereroberfläche hergestellt.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Gibt an, dass es sich hierbei um ein einfaches Update handelt, das keine Zeiger Zustandsänderungen einschließt.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Gibt an, dass dieser Zeiger in den Zustand "up" übergeht. Das heißt, der Kontakt mit der digitalisiereroberfläche wurde beendet.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Gibt Eingaben an, die einem zeigerrad zugeordnet sind. Bei Maus Zeigern entspricht dies der Aktion des Mausrades ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Gibt Eingaben an, die einem Zeiger-h-Rad zugeordnet sind. Bei Maus Zeigern entspricht dies der Aktion des horizontalen Mausrads ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Gibt an, dass dieser Zeiger von einem anderen Element (zugeordnet) aufgezeichnet und das ursprüngliche Element die Erfassung verloren hat (siehe [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Gibt an, dass dieser Zeiger über eine zugeordnete Transformation verfügt.


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

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**POINTER_BUTTON_CHANGE_TYPE**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

