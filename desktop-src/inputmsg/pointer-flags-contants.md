---
title: Zeigerflags
description: Werte, die im pointerFlags-Feld der POINTER_INFO-Struktur angezeigt werden können.
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
ms.openlocfilehash: 0ae56ebfc016b0e4497db7cc998753189ce36a87962c0305962800ad133e8bca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482036"
---
# <a name="pointer-flags"></a>Zeigerflags

Werte, die im **pointerFlags-Feld** der [**POINTER_INFO-Struktur**](/previous-versions/windows/desktop/api) angezeigt werden können.

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



Gibt an, dass dieser Zeiger weiterhin vorhanden ist. Wenn dieses Flag nicht festgelegt ist, gibt es an, dass der Zeiger über den linken Erkennungsbereich verfügt.

Dieses Flag wird in der Regel nicht nur festgelegt, wenn ein zeigerender Zeiger den Erkennungsbereich verlässt **(POINTER_FLAG_UPDATE** festgelegt ist) oder wenn ein Zeiger in Kontakt mit einer Fensteroberfläche den Erkennungsbereich verlässt (**POINTER_FLAG_UP** festgelegt ist).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Gibt an, dass dieser Zeiger mit der Digitizeroberfläche in Kontakt steht. Wenn dieses Flag nicht festgelegt ist, gibt es einen Zeigenzeiger an.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Gibt eine primäre Aktion analog zu einer linken Maustaste nach unten an.

Für einen Touchzeiger ist dieses Flag festgelegt, wenn es mit der Digitizeroberfläche in Kontakt steht.

Für einen Stiftzeiger ist dieses Flag festgelegt, wenn es mit der Digitizeroberfläche in Kontakt steht und keine Schaltflächen gedrückt werden.

Für einen Mauszeiger ist dieses Flag festgelegt, wenn die linke Maustaste gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Gibt eine sekundäre Aktion analog zu einer rechten Maustaste nach unten an.

Ein Berührungszeiger verwendet dieses Flag nicht.

Für einen Stiftzeiger ist dieses Flag festgelegt, wenn es mit der Digitizeroberfläche in Kontakt steht und die Stiftschaltfläche gedrückt wird.

Für einen Mauszeiger ist dieses Flag festgelegt, wenn die rechte Maustaste gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Analog zu einer Mausradschaltfläche nach unten.

Ein Berührungszeiger verwendet dieses Flag nicht.

Ein Stiftzeiger verwendet dieses Flag nicht.

Für einen Mauszeiger ist dieses Flag festgelegt, wenn das Mausrad gedrückt ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Analog zu einer ersten erweiterten Mausschaltfläche (XButton1) nach unten.

Ein Berührungszeiger verwendet dieses Flag nicht.

Ein Stiftzeiger verwendet dieses Flag nicht.

Für einen Mauszeiger ist dieses Flag festgelegt, wenn die erste erweiterte Mausschaltfläche (XBUTTON1) ausgeschaltet ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Analog zu einer zweiten erweiterten Mausschaltfläche (XButton2) nach unten.

Ein Berührungszeiger verwendet dieses Flag nicht.

Ein Stiftzeiger verwendet dieses Flag nicht.

Für einen Mauszeiger ist dieses Flag festgelegt, wenn die zweite erweiterte Mausschaltfläche (XBUTTON2) ausgeschaltet ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Gibt an, dass dieser Zeiger als primärer Zeiger festgelegt wurde. Ein primärer Zeiger ist ein einzelner Zeiger, der Aktionen ausführen kann, die über diejenigen hinausgehen, die für nicht primäre Zeiger verfügbar sind. Wenn beispielsweise ein primärer Zeiger Kontakt mit der Oberfläche eines Fensters nimmt, kann er dem Fenster die Möglichkeit geben, sich zu aktivieren, indem er eine [**WM_POINTERACTIVATE**](wm-pointeractivate.md) Nachricht sendet.

Der primäre Zeiger wird aus allen aktuellen Benutzerinteraktionen auf dem System identifiziert (Maus, Fingereingabe, Stift usw.). Daher ist der primäre Zeiger ihrer App möglicherweise nicht zugeordnet. Der erste Kontakt in einer Multitouch-Interaktion wird als primärer Zeiger festgelegt. Sobald ein primärer Zeiger identifiziert wurde, müssen alle Kontakte aufgehoben werden, bevor ein neuer Kontakt als primärer Zeiger identifiziert werden kann. Für Apps, die zeigereingaben nicht verarbeiten, werden nur die Ereignisse des primären Zeigers zu Mausereignissen heraufgestuft.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**
</dt> <dd> <dl> <dt>

0x000004000
</dt> <dt>



Vertrauen ist ein Vorschlag des Quellgeräts, ob der Zeiger eine beabsichtigte oder versehentliche Interaktion darstellt. Dies ist besonders relevant für PT_TOUCH Zeiger, bei denen eine versehentliche Interaktion (z. B. mit der Handfläche) Eingaben auslösen kann. Das Vorhandensein dieses Flags gibt an, dass das Quellgerät sehr sicher ist, dass diese Eingabe Teil einer beabsichtigten Interaktion ist.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**
</dt> <dd> <dl> <dt>

0x000008000
</dt> <dt>



Gibt an, dass der Zeiger auf ungewöhnliche Weise abweicht, z. B. wenn das System ungültige Eingaben für den Zeiger empfängt oder wenn ein Gerät mit aktiven Zeigern plötzlich ausfällt. Wenn die Anwendung, die die Eingabe empfängt, dazu in der Lage ist, sollte sie die Interaktion als nicht abgeschlossen behandeln und alle Auswirkungen des betreffenden Zeigers umkehren.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Gibt an, dass dieser Zeiger in einen Abwärtszustand übergewechselt wurde. Das heißt, es hat Kontakt mit der Digitizeroberfläche hergestellt.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Gibt an, dass dies ein einfaches Update ist, das keine Zeigerzustandsänderungen enthält.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Gibt an, dass dieser Zeiger in einen Auf-Zustand übergewechselt wurde. Das heißt, der Kontakt mit der Digitizeroberfläche wurde beendet.


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



Gibt die Eingabe an, die einem Zeigerrad zugeordnet ist. Bei Mauszeigern entspricht dies der Aktion des Mausrades ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Gibt die Eingabe an, die einem Zeiger-H-Wheel zugeordnet ist. Bei Mauszeigern entspricht dies der Aktion des horizontalen Mausrades ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Gibt an, dass dieser Zeiger von (zugeordnet) einem anderen Element erfasst wurde und das ursprüngliche Element die Erfassung verloren hat (siehe [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).


</dt> </dl> </dd> <dt>

<span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Gibt an, dass diesem Zeiger eine Transformation zugeordnet ist.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

XBUTTON1 und XBUTTON2 sind zusätzliche Schaltflächen, die auf vielen Mausgeräten verwendet werden. Sie geben die gleichen Daten wie Standard-Maustasten zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Konstanten](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> <dt>

[**POINTER_BUTTON_CHANGE_TYPE**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

