---
description: Tritt auf, wenn eine Anwendungs Geste erkannt wird.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: InkEdit. Gesten-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216594"
---
# <a name="inkeditgesture-event"></a>InkEdit. Gesten-Ereignis

Tritt auf, wenn eine Anwendungs Geste erkannt wird.

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

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das zum Erstellen dieser Geste verwendet wurde.

</dd> <dt>

*Striche* \[ in\]
</dt> <dd>

Die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die die [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte enthält, die diese Geste bilden.

</dd> <dt>

*Gesten* \[ in\]
</dt> <dd>

Ein Array von [**iinkgesten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) -Objekten in der richtigen Reihenfolge.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

Gibt an, ob die [inkstroke](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, aus der diese Geste besteht, abgebrochen werden soll, um die frei Hand Eingabe zu löschen und das [**Stroke**](inkedit-stroke.md) -Ereignis auszulösen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert. Die **\_ iinkeditevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner DISPID \_ ieegesten.

Ein **Gesten** Ereignis wird nur ausgelöst, wenn das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt für das [**iinkgesten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) -Objekt das erste **IInkStrokeDisp** -Objekt seit dem letzten aufzurufenden [**Rückruf der Erkennungsmethode oder**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) der letzten Auslösung des Erkennungs Timeouts ist.

Wenn das **Gesten** Ereignis abgebrochen wird, wird das [**Stroke**](inkedit-stroke.md) -Ereignis für die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ausgelöst, die das **Gesten** Ereignis ausgelöst hat.

Damit dieses Ereignis auftritt, muss das [InkEdit](inkedit-control-reference.md) -Steuerelement einen Satz von Anwendungs Gesten abonnieren. Um das Interesse des InkEdit-Steuer Elements in einem Satz von Gesten festzulegen, müssen Sie die [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) -Methode aufrufen.

Eine Liste der Anwendungs Gesten finden Sie unter der [**inkapplicationgesten-Enumerationstyp**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

Das [InkEdit](inkedit-control-reference.md) -Steuerelement erkennt nicht mehrere Strich Gesten.

Das [InkEdit](inkedit-control-reference.md) -Steuerelement abonniert die folgenden Gesten.



| Geste                              | Aktion               |
|--------------------------------------|----------------------|
| Nach unten links, nach unten links<br/> | EINGABETASTE<br/>     |
| Rechts<br/>                     | LeerZchn<br/>     |
| Links<br/>                      | Rücktaste<br/> |
| Rechts oben, rechts oben<br/>   | Registerkarte<br/>       |



 

So ändern Sie die Standardaktion für eine Geste:

1.  Fügen Sie Ereignishandler für die **Gesten** -und [**hubereignisse**](inkedit-stroke.md) hinzu.
2.  Brechen Sie im **Gesten** Ereignishandler das **Gesten** Ereignis für die Geste ab, und führen Sie die alternative Aktion für die Geste aus.
3.  Brechen Sie im [**Stroke**](inkedit-stroke.md) -Ereignishandler das **Stroke** -Ereignis für das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt ab, das das abgebrochene **Gesten** Ereignis ausgelöst hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Inkapplicationgesten-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**SetGestureStatus-Methode, \[ InkEdit-Steuerelement\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)
</dt> <dt>

[**RecoTimeout (Eigenschaft)**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

[**InkEdit-Steuerelement für Stroke-Ereignis \[\]**](inkedit-stroke.md)
</dt> <dt>

[Verwenden von Gesten](using-gestures.md)
</dt> </dl>

 

