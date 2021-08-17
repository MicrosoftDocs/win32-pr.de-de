---
description: Setzt den Enumerationsverweis auf das erste IWiaItem2-Objekt zurück.
ms.assetid: 392e3471-f7fc-456f-a1cc-ab4eb6d3fe18
title: IEnumWiaItem2::Reset-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Reset
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4811ab00cc842712502556a4ab8a315b6b6780031e7fc52852f9a3b6fdde96b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451120"
---
# <a name="ienumwiaitem2reset-method"></a>IEnumWiaItem2::Reset-Methode

Setzt den Enumerationsverweis auf das erste [**IWiaItem2-Objekt**](-wia-iwiaitem2.md) zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




