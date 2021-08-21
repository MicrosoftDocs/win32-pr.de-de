---
description: Tritt ein, wenn eine Anwendungsgeste erkannt wird.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: InkEdit.Gesture-Ereignis (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a718106f4485682a1b6267f942ec3ef0f5a9fb670449e1f6023d86a5b03af56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032078"
---
# <a name="inkeditgesture-event"></a>InkEdit.Gesture-Ereignis

Tritt ein, wenn eine Anwendungsgeste erkannt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das zum Erstellen dieser Geste verwendet wurde.

</dd> <dt>

*Striche* \[ In\]
</dt> <dd>

Die [InkStrokes-Sammlung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) die die [**IInkStrokeDisp-Objekte**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) enthält, aus denen diese Geste besteht.

</dd> <dt>

*Gesten* \[ In\]
</dt> <dd>

Ein Array von [**IInkGesture-Objekten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) in der Reihenfolge der Konfidenz.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

Gibt an, ob die [InkStrokes-Sammlung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) die diese Geste bildet, abgebrochen werden soll, damit die Ink-Sammlung nicht gelöscht und das [**Stroke-Ereignis**](inkedit-stroke.md) ausgelöst wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in der **\_ IInkEditEvents-Schnittstelle** definiert. Die **\_ IInkEditEvents-Schnittstelle** implementiert die IDispatch-Schnittstelle mit dem Bezeichner DISPID \_ IeeGesture.

Ein **Gestenereignis** wird nur ausgelöst, wenn [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) für das [**IInkGesture-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) das erste **IInkStrokeDisp-Objekt** seit dem letzten Aufruf der [**Recognize-Methode**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) oder dem letzten Auslösen des Erkennungstimeouts ist.

Wenn das **Gesture-Ereignis** abgebrochen wird, wird das [**Stroke-Ereignis**](inkedit-stroke.md) für die [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ausgelöst, die das **Gesture-Ereignis** ausgelöst hat.

Damit dieses Ereignis eintritt, muss das [InkEdit-Steuerelement](inkedit-control-reference.md) eine Reihe von Anwendungsgesten abonnieren. Um das Interesse des InkEdit-Steuerelements an einer Reihe von Gesten festzulegen, rufen Sie die [**SetGestureStatus-Methode**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) auf.

Eine Liste der Anwendungsgesten finden Sie unter [**InkApplicationGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)

Das [InkEdit-Steuerelement](inkedit-control-reference.md) erkennt nicht mehrere Strichgesten.

Das [InkEdit-Steuerelement](inkedit-control-reference.md) abonniert die folgenden Gesten.



| Geste                              | Aktion               |
|--------------------------------------|----------------------|
| Links unten, links unten– lang<br/> | EINGABETASTE<br/>     |
| Right<br/>                     | LeerZchn<br/>     |
| Links<br/>                      | Rückschritt<br/> |
| Up-right, Up-right-long<br/>   | Registerkarte<br/>       |



 

So ändern Sie die Standardaktion für eine Geste:

1.  Fügen Sie Ereignishandler für die **Gesten-** und [**Strichereignisse**](inkedit-stroke.md) hinzu.
2.  Brechen Sie im **Gestenereignishandler** das **Gestenereignis** für die Geste ab, und führen Sie die alternative Aktion für die Geste aus.
3.  Brechen [](inkedit-stroke.md) Sie im Stroke-Ereignishandler das **Stroke-Ereignis** für das [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ab, das das abgebrochene **Gesture-Ereignis** ausgelöst hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (erfordert auch inked \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> <dt>

[**InkApplicationGesture-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**SetGestureStatus-Methode \[ inkEdit-Steuerelement\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)
</dt> <dt>

[**RecoTimeout-Eigenschaft**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

[**Stroke Event \[ InkEdit-Steuerelement\]**](inkedit-stroke.md)
</dt> <dt>

[Verwenden von Gesten](using-gestures.md)
</dt> </dl>

 

