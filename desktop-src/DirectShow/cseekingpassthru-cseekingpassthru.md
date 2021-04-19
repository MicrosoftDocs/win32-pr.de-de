---
description: Konstruktormethode.
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: Cseekingpassthru. cseekingpassthru-Konstruktor (seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a93ed9706762b9a1672bfae85550ee4c2aceeead
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352834"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a>Cseekingpassthru. cseekingpassthru-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeichenfolge, die den Namen des Objekts enthält. Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md) .

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts. Andernfalls legen Sie diesen Parameter auf **null** fest.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert. Ignoriert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Seekpt. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cseekingpassthru-Klasse**](cseekingpassthru.md)
</dt> </dl>

 

 




