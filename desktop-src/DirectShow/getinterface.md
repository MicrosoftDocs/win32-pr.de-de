---
description: Die GetInterface-Funktion ruft einen Schnittstellenzeiger ab.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: GetInterface-Funktion (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 289c6e56d4b5387fe9224e476c69865107102141b687825cdfd9a717f482632c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537030"
---
# <a name="getinterface-function"></a>GetInterface-Funktion

Die `GetInterface` Funktion ruft einen Schnittstellenzeiger ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Punk* 
</dt> <dd>

Zeiger auf die **IUnknown-Schnittstelle.**

</dd> <dt>

*Ppv* 
</dt> <dd>

Adresse eines Zeigers auf die abgerufene Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion führt ein threadsicheres Inkrement des Verweiszählers aus. Um die Schnittstelle abzurufen und einen Verweis hinzuzufügen, rufen Sie diese Funktion aus Ihrer überschreibenden Implementierung der **INonDelegatingUnknown::NonDelegatingQueryInterface-Methode auf.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COM-Hilfsfunktionen**](com-helper-functions.md)
</dt> <dt>

[**INonDelegatingUnknown**](inondelegatingunknown.md)
</dt> </dl>

 

 




