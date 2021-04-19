---
description: Erfahren Sie mehr über die Konstruktormethode cmediaposition. cmediaposition (ctlutil. h). Diese Methode verwendet die Parameter "pname", "Punk" und "PHR".
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: Cmediaposition. cmediaposition-Konstruktor (ctlutil. h)
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
ms.openlocfilehash: cb9d86a2403cd0e2e71130b51cdb87bad15c4e95
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106363191"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a>Cmediaposition. cmediaposition-Konstruktor (ctlutil. h)-pName, Punk, PHR-Parameter

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
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

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert.

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

 

 




