---
description: Die TakePicture-Methode des Item-Objekts bewirkt, dass ein Digitalkameragerät ein Bild macht und ein Item-Objekt zurückgibt, das das resultierende Bild darstellt. Diese Methode gilt nur für Digitalkamerageräte.
ms.assetid: d181048e-21ef-4fcc-a50a-5ba44bbde72e
title: Item.TakePicture-Methode (Wiavideo.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.TakePicture
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: e7d2e67876cd32b1db2181aba491090d44679756f5503c078d1edff495afc1cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440588"
---
# <a name="itemtakepicture-method"></a>Item.TakePicture-Methode

Die **TakePicture-Methode** des [**Item-Objekts**](-wia-item.md) bewirkt, dass ein Digitalkameragerät ein Bild macht und ein **Item-Objekt** zurückgibt, das das resultierende Bild darstellt. Diese Methode gilt nur für Digitalkamerageräte.

## <a name="syntax"></a>Syntax


```JScript
retVal = Item.TakePicture()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **IWiaDispatchItem**

Ein [**Item-Objekt,**](-wia-item.md) das das von dieser Methode erstellte Bild darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wiavideo.h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




