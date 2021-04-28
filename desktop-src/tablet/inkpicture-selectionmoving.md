---
description: 'InkPicture.SelectionMoving-Ereignis: Tritt ein, wenn sich die Position der aktuellen Auswahl ändert, z. B. durch Änderungen an der Benutzeroberfläche, Ausschneide- und Einfügeprozeduren oder die Selection-Eigenschaft.'
ms.assetid: 310003a1-f282-4efa-9a75-c575a9193a77
title: InkPicture.SelectionMoving-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eee50fe1115ce72dff0674ad4e6c2457500c7de8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086458"
---
# <a name="inkpictureselectionmoving-event"></a>InkPicture.SelectionMoving-Ereignis

Tritt ein, wenn sich die Position der aktuellen Auswahl ändert, z. B. durch Änderungen [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) an der Benutzeroberfläche, Prozeduren zum Ausschneiden und Einfügen oder die Selection-Eigenschaft.

## <a name="syntax"></a>Syntax


```C++
void SelectionMoving(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CurSelectionRect* \[ In\]
</dt> <dd>

Das Rechteck, in das die Auswahl nach dem **SelectionMoving-Ereignis** verschoben wird.

> [!Note]  
> Dieses Rechteck wird in Clientfensterkoordinaten angegeben, was Szenarien wie das Beibehalten des Seitenverhältnisses bei der Größenänderung ermöglicht.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ IOESelectionMoving definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**Selection Property \[ InkPicture-Steuerelement\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> <dt>

[**InkRectangle-Klasse**](inkrectangle-class.md)
</dt> </dl>

 

 




