---
description: 'InkOverlay.SelectionMoved-Ereignis: Tritt auf, wenn sich die Position der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, Durchschneide- und Einfügevorgänge oder die Selection-Eigenschaft.'
ms.assetid: 78b5ab11-01c0-4bdb-ae1f-ec55774abdce
title: InkOverlay.SelectionMoved-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e1c9501a9670ebfa89cdcf30fac7a1044450cef932e7c7abb522a5199fd47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032068"
---
# <a name="inkoverlayselectionmoved-event"></a>InkOverlay.SelectionMoved-Ereignis

Tritt ein, wenn sich die Position der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die [**Selection-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

## <a name="syntax"></a>Syntax


```C++
void SelectionMoved(
  [in] IInkRectangle *OldSelectionRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OldSelectionRect* \[ In\]
</dt> <dd>

Das umgebundene Rechteck der ausgewählten [InkStrokes-Auflistung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wie es vor dem **Ausgelösten des SelectionMoved-Ereignisses vorhanden** war.

> [!Note]  
> Dieses Rechteck wird in Freiraumkoordinaten angegeben, was Rückgängig-Szenarien ermöglicht.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die TThis-Ereignismethode wird in den \_ \_ dispatch-only-Schnittstellen (dispinterfaces) von IInkOverlayEvents und IInkPictureEvents mit der ID DISPID \_ IOESelectionMoved definiert.

Um das neue umgebundene Rechteck der Auflistung der verschobenen Striche zu erhalten, rufen Sie die [**Selection.GetBoundingBox-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**Selection-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> <dt>

[**InkRectangle-Klasse**](inkrectangle-class.md)
</dt> </dl>

 

