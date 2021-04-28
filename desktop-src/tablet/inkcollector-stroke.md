---
description: 'InkCollector.Stroke-Ereignis: Tritt auf, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.'
ms.assetid: eaa89dfe-6141-4205-845b-634321130e26
title: InkCollector.Stroke-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49cb90b02ab3fca60a8fa17089b6a76f959a60e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110055"
---
# <a name="inkcollectorstroke-event"></a>InkCollector.Stroke-Ereignis

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

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das Stroke-Ereignis **generiert** hat.

</dd> <dt>

*Strich* \[ In\]
</dt> <dd>

Das [**gesammelte IInkStrokeDisp-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

**VARIANT \_ TRUE zum** Abbrechen des Ereignisses; andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICEStroke definiert.

Das **Stroke-Ereignis** wird ausgelöst, wenn es sich im Auswahl- oder Löschmodus befindet, nicht nur beim Einfügen von Ink. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein größeres Bewusstsein für Plattformereignisse.

> [!Note]  
> Das **Stroke-Ereignis** wird beim Zeichnen eines Strichs durch den Benutzer und nicht beim Hinzugefügt eines Strichs zur [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) angezeigt. Wenn der Benutzer zum ersten Mal mit dem Zeichnen eines Strichs beginnt, wird er sofort der InkStrokes-Auflistung hinzugefügt. Das **Stroke-Ereignis** wird jedoch erst dann aus, wenn der Strich abgeschlossen ist. Daher können Striche in der InkStrokes-Auflistung vorhanden sein, die der **Stroke-Ereignishandler** nicht gesehen hat.

 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**StrokesAdded Event \[ InkStrokes Collection\]**](inkstrokes-strokesadded.md)
</dt> <dt>

[**StrokesDeleted-Ereignis \[ inkOverlay-Klasse\]**](inkoverlay-strokesdeleted.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

