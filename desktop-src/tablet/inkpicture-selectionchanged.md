---
description: Tritt ein, wenn sich die Auswahl von Freihand im InkPicture-Steuerelement geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, Ausschneide- und Einfügeprozeduren oder die Selection-Eigenschaft.
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: InkPicture.SelectionChanged-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1fce27d9aa0dd043c5e474d790c1bd9737a9c10bffbed3eff6a287be67030f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939000"
---
# <a name="inkpictureselectionchanged-event"></a>InkPicture.SelectionChanged-Ereignis

Tritt ein, wenn sich die Auswahl von Freihand im [InkPicture-Steuerelement](inkpicture-control-reference.md) geändert hat, z. B. durch Änderungen an der Benutzeroberfläche, Ausschneide- und Einfügeprozeduren oder die [**Selection-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)

## <a name="syntax"></a>Syntax


```C++
void SelectionChanged();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Weitere Informationen zu diesem Ereignis finden Sie im [**SelectionChanged-Ereignis**](inkoverlay-selectionchanged.md) des [**InkOverlay-Objekts,**](inkoverlay-class.md) das über die gleiche Funktionalität verfügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> <dt>

[**Selection Property \[ InkPicture-Steuerelement\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)
</dt> </dl>

 

 




