---
description: Erfahren Sie mehr über die CMediaPosition.CMediaPosition (Ctlutil.h)-Konstruktormethode. Diese Methode verwendet die Parameter "pName" und "pUnk".
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: CMediaPosition.CMediaPosition-Konstruktor (Ctlutil.h)- pName, pUnk-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0df3337c07ed678354515bdf0c665a5d6157f158ac6c2370a8981d8e5028b27e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634794"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a>CMediaPosition.CMediaPosition-Konstruktor (Ctlutil.h) – pName, pUnk-Parameter

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeiger auf den Namen des Objekts zu Debugzwecken. Ordnen Sie diesen Parameter im statischen Speicher zu.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts oder **NULL,** wenn das Objekt nicht aggregiert wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Ctlutil.h (include Streams.h) |
| Bibliothek| Strmbase.lib (Verkaufsbuilds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaPosition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




