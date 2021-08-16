---
description: 'InkOverlay.SelectionResized-Ereignis: Tritt ein, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, Ausschneide- und Einfügeprozessen oder die Selection-Eigenschaft.'
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: InkOverlay.SelectionResized-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39b5de8e38dc9b11fcd3e46c26a7970181c97d3af07864e346c0e30a2d829f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218646"
---
# <a name="inkoverlayselectionresized-event"></a>InkOverlay.SelectionResized-Ereignis

Tritt ein, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) durch Änderungen an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.

## <a name="syntax"></a>Syntax


```C++
void SelectionResized(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OldSelectionRect* \[ In\]
</dt> <dd>

Das umschließende Rechteck der ausgewählten [InkStrokes-Auflistung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wie es vor dem **Ausgelösten SelectionResized-Ereignis** vorhanden war.

> [!Note]  
> Dieses Rechteck wird in Freihandraumkoordinaten angegeben, was Rückgängig-Szenarien ermöglicht.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IOESelectionResized definiert.

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

[**Selection-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**InkRectangle-Klasse**](inkrectangle-class.md)
</dt> </dl>

 

