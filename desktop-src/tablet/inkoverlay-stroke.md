---
description: Tritt ein, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: InkOverlay. Stroke-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6db3bdbe996830596a8e25cebf6f05b94638894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759529"
---
# <a name="inkoverlaystroke-event"></a>InkOverlay. Stroke-Ereignis

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

*Cursor* \[ in\]
</dt> <dd>

Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das [**Stroke**](inkcollector-stroke.md) -Ereignis generiert hat.

</dd> <dt>

*Strich* \[ in\]
</dt> <dd>

Das gesammelte [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt.

</dd> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

Gibt an, ob das Ereignis abgebrochen werden soll. **True** gibt an, dass die Auflistung des Strichs abgebrochen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icestroke definiert.

Das [**Stroke**](inkcollector-stroke.md) -Ereignis wird im Modus zum auswählen oder löschen ausgelöst, nicht nur beim Einfügen von frei Hand Eingaben. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.

> [!Note]  
> Das [**Stroke**](inkcollector-stroke.md) -Ereignis wird ausgelöst, wenn der Benutzer das Zeichnen eines Strichs beendet, nicht, wenn der [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ein Strich hinzugefügt wird. Wenn der Benutzer erstmalig mit dem Zeichnen eines Strichs beginnt, wird er sofort der inkstrokes-Auflistung hinzugefügt. Das **Stroke** -Ereignis wird jedoch erst ausgelöst, wenn der Strich beendet ist. Daher können Striche in der inkstrokes-Auflistung vorhanden sein, die der **Stroke** -Ereignishandler nicht gesehen hat.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**StrokesAdded-Auflistung für Ereignis \[ inkstrokes\]**](inkstrokes-strokesadded.md)
</dt> <dt>

[**StrokesDeleted-Ereignis \[ InkOverlay-Klasse\]**](inkoverlay-strokesdeleted.md)
</dt> <dt>

[**Iinkcursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

