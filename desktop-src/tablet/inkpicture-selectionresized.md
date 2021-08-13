---
description: 'InkPicture.SelectionResized-Ereignis: Tritt auf, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, Durchschneide- und Einfügevorgänge oder die Selection-Eigenschaft.'
ms.assetid: 4e7f461f-2909-40ab-98d8-b763d489eb62
title: InkPicture.SelectionResized-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e67bc19d4d35c356e0774f0843ba62432606c1ee4f1f84095e64c4808d09bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451053"
---
# <a name="inkpictureselectionresized-event"></a>InkPicture.SelectionResized-Ereignis

Tritt ein, wenn sich die Größe der aktuellen Auswahl geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die [**Selection-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)

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

Das umgebundene Rechteck der ausgewählten [InkStrokes-Auflistung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wie es vor dem **Ereignis SelectionResized vorhanden** war.

> [!Note]  
> Dieses Rechteck wird in Freiraumkoordinaten angegeben, was Rückgängig-Szenarien ermöglicht.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den dispatch-only-Schnittstellen (dispinterfaces) **\_ von IInkOverlayEvents** und **\_ IInkPictureEvents** mit der ID DISPID \_ IOESelectionResized definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**Selection Property \[ InkPicture-Steuerelement\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> <dt>

[**InkRectangle-Klasse**](inkrectangle-class.md)
</dt> </dl>

 

