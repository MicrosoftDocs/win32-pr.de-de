---
description: Die takepicture-Methode des Item-Objekts bewirkt, dass ein digitales Kamera Gerät ein Bild annimmt und ein Element Objekt zurückgibt, das das resultierende Bild darstellt. Diese Methode gilt nur für digitale Kamerageräte.
ms.assetid: d181048e-21ef-4fcc-a50a-5ba44bbde72e
title: Item. takepicture-Methode (WiaVideo. h)
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
ms.openlocfilehash: fd07f7ccd4f2c65c2d911dabdd0ca829dc241765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959819"
---
# <a name="itemtakepicture-method"></a>Item. takepicture-Methode

Die **takepicture** -Methode des [**Item**](-wia-item.md) -Objekts bewirkt, dass ein digitales Kamera Gerät ein Bild annimmt und ein **Element** Objekt zurückgibt, das das resultierende Bild darstellt. Diese Methode gilt nur für digitale Kamerageräte.

## <a name="syntax"></a>Syntax


```JScript
retVal = Item.TakePicture()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **iwiadispatchitem**

Ein [**Element**](-wia-item.md) Objekt, das das Bild darstellt, das von dieser Methode erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>WiaVideo. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




