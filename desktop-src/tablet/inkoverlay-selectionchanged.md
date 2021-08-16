---
description: Tritt ein, wenn sich die Auswahl der Freifläche innerhalb des Steuerelements geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die Selection-Eigenschaft.
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: InkOverlay.SelectionChanged-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bbe4e239b1100277adea0b784a93bf16bf8497cfd8dd44877f7fe7e3fd7652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218973"
---
# <a name="inkoverlayselectionchanged-event"></a>InkOverlay.SelectionChanged-Ereignis

Tritt ein, wenn sich die Auswahl der Freifläche innerhalb des Steuerelements geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, durch Ausschneide- und Einfügevorgänge oder durch die [**Selection-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)

## <a name="syntax"></a>Syntax


```C++
void SelectionChanged();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Es gibt keine Ereignisdaten.

Diese Ereignismethode wird in den \_ \_ dispatch-only-Schnittstellen (dispinterfaces) von IInkOverlayEvents und IInkPictureEvents mit der ID DISPID \_ IOESelectionChanged definiert.

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
</dt> </dl>

 

 




