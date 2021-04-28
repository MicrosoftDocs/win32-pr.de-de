---
description: 'InkOverlay.SelectionResized-Ereignis: Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die Selection-Eigenschaft.'
ms.assetid: 606d4bdf-b02e-459f-a4cf-050daac6c309
title: InkOverlay.SelectionResized-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f3dd3cf1bdda004733dde99bb66150710044310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116878"
---
# <a name="inkoverlayselectionresized-event"></a>InkOverlay.SelectionResized-Ereignis

Tritt ein, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die [**Selection-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

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

Das umgebundene Rechteck der ausgewählten [InkStrokes-Auflistung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wie es vor dem **Ausgelösten SelectionResized-Ereignis vorhanden** war.

> [!Note]  
> Dieses Rechteck wird in Freiraumkoordinaten angegeben, was Rückgängig-Szenarien ermöglicht.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den \_ \_ dispatch-only-Schnittstellen (dispinterfaces) von IInkOverlayEvents und IInkPictureEvents mit der ID DISPID \_ IOESelectionResized definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]<br/>                                                       |
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

 

