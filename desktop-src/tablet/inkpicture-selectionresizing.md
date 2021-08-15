---
description: 'InkPicture.SelectionResizing-Ereignis: Tritt auf, wenn sich die Größe der aktuellen Auswahl ändern wird, z. B. durch Änderungen an der Benutzeroberfläche, Durchschneide- und Einfügevorgänge oder die Selection-Eigenschaft.'
ms.assetid: da708712-2773-45f5-9d9b-49fabe7fdb5a
title: InkPicture.SelectionResizing-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caeae852802599a401c1cdff97436672e0cbfe252f8f1e96d6f4c98367c828ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966959"
---
# <a name="inkpictureselectionresizing-event"></a>InkPicture.SelectionResizing-Ereignis

Tritt ein, wenn sich die Größe der aktuellen Auswahl ändern wird, z. B. durch Änderungen [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die Selection-Eigenschaft.

## <a name="syntax"></a>Syntax


```C++
void SelectionResizing(
  [in] IInkRectangle *CurSelectionRect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CurSelectionRect* \[ In\]
</dt> <dd>

Das umgebundene Rechteck der Auswahl nach dem **SelectionResizing-Ereignis.**

> [!Note]  
> Dieses Rechteck wird in Clientfensterkoordinaten angegeben, was Szenarien wie das Beibehalten des Seitenverhältnisses beim Ändern der Größe ermöglicht.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in den dispatch-only-Schnittstellen (dispinterfaces) **\_ von IInkOverlayEvents** und **\_ IInkPictureEvents** mit der ID DISPID \_ IOESelectionResizing definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
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

 

 




