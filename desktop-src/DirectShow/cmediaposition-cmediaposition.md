---
description: Erfahren Sie mehr über die Konstruktormethode cmediaposition. cmediaposition (ctlutil. h). Diese Methode verwendet die Parameter "pname" und "Punk".
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: Cmediaposition. cmediaposition-Konstruktor (ctlutil. h)-pName, Punk-Parameter
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
ms.openlocfilehash: e65f034e5f8857b21bc706bce45aa74c3c3cf966
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106369345"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a>Cmediaposition. cmediaposition-Konstruktor (ctlutil. h)-pName, Punk-Parameter

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

Zeiger auf den Namen des Objekts, zu Debuggingzwecken. Weisen Sie diesen Parameter im statischen Arbeitsspeicher zu.

</dd> <dt>

*Kro* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts oder **null** , wenn das Objekt nicht aggregiert wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Ctlutil. h (Include Streams. h) |
| Bibliothek| "Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediaposition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




