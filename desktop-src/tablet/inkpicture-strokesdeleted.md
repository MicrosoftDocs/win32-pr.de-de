---
description: Tritt ein, nachdem IInkStrokeDisp-Objekte aus der Ink-Eigenschaft gelöscht wurden.
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: InkPicture.StrokesDeleted-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b2d4f0be69adf6c9c44f3eadec250d8cba3ebb8935bde5c06cd026e478da3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717359"
---
# <a name="inkpicturestrokesdeleted-event"></a>InkPicture.StrokesDeleted-Ereignis

Tritt ein, nachdem [**IInkStrokeDisp-Objekte**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) aus der [**Ink-Eigenschaft gelöscht**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) wurden.

## <a name="syntax"></a>Syntax


```C++
void StrokesDeleted();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Es gibt keine Ereignisdaten.

Diese Ereignismethode wird in den dispatch-only-Schnittstellen (dispinterfaces) **\_ von IInkOverlayEvents** und **\_ IInkPictureEvents** mit der ID DISPID \_ IOEStrokesDeleted definiert.

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
</dt> </dl>

 

 




