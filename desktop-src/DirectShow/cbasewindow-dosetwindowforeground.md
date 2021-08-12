---
description: Die DoSetWindowForeground-Methode bringt das Fenster in den Vordergrund.
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: CBaseWindow.DoSetWindowForeground-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoSetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f0d0dd99f5e2c5e5afffb78066a9380c56f744a4ba54b64bf987df15ea58862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658019"
---
# <a name="cbasewindowdosetwindowforeground-method"></a>CBaseWindow.DoSetWindowForeground-Methode

Die `DoSetWindowForeground` -Methode bringt das Fenster in den Vordergrund.

## <a name="syntax"></a>Syntax


```C++
void DoSetWindowForeground(
   BOOL bFocus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bFocus* 
</dt> <dd>

Boolescher Wert, der angibt, ob das Fenster den Fokus erhalten soll. Wenn der Wert **TRUE ist,** erhält das Fenster den Fokus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




