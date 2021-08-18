---
description: 'InkOverlay.Stroke-Ereignis: Tritt auf, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.'
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: InkOverlay.Stroke-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2836699591b4f1a87ce3d206a795eb13be188def28ea3eadef687a1d96024ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712630"
---
# <a name="inkoverlaystroke-event"></a>InkOverlay.Stroke-Ereignis

Tritt ein, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.

## <a name="syntax"></a>Syntax


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**Stroke-Ereignis**](inkcollector-stroke.md) generiert hat.

</dd> <dt>

*Strich* \[ In\]
</dt> <dd>

Das gesammelte [**IInkStrokeDisp-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

Gibt an, ob das Ereignis abgebrochen werden soll. True gibt an, dass die Auflistung des Strichs abgebrochen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICEStroke definiert.

Das [**Stroke-Ereignis**](inkcollector-stroke.md) wird beim Auswählen oder Löschen ausgelöst, nicht nur beim Einfügen von Ink. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein höheres Bewusstsein für Plattformereignisse.

> [!Note]  
> Das [**Stroke-Ereignis**](inkcollector-stroke.md) wird ausgelöst, wenn der Benutzer das Zeichnen eines Strichs beendet, nicht, wenn der [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) ein Strich hinzugefügt wird. Wenn der Benutzer zum ersten Mal einen Strich zeichnet, wird er sofort der Sammlung InkStrokes hinzugefügt. das **Stroke-Ereignis** wird jedoch erst ausgelöst, wenn der Strich abgeschlossen ist. Daher können Striche in der InkStrokes-Auflistung vorhanden sein, die der **Stroke-Ereignishandler** nicht gesehen hat.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**StrokesAdded Event \[ InkStrokes Collection\]**](inkstrokes-strokesadded.md)
</dt> <dt>

[**StrokesDeleted-Ereignis \[ inkOverlay-Klasse\]**](inkoverlay-strokesdeleted.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

