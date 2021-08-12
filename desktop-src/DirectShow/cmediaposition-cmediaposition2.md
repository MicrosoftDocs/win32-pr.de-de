---
description: Erfahren Sie mehr über die CMediaPosition.CMediaPosition (Ctlutil.h)-Konstruktormethode. Diese Methode verwendet die Parameter "pName", "pUnk" und "phr".
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: CMediaPosition.CMediaPosition-Konstruktor (Ctlutil.h)
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
ms.openlocfilehash: 101678ebcb851ef0fcdc8eeaa202435ca80eb796555c81e5e5d95eb4998131c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655261"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a>CMediaPosition.CMediaPosition-Konstruktor (Ctlutil.h) – pName, pUnk, phr-Parameter

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

Zeiger auf den Namen des Objekts zu Debugzwecken. Ordnen Sie diesen Parameter im statischen Speicher zu.

</dd> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts oder **NULL,** wenn das Objekt nicht aggregiert ist.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-|-|
| Header | Ctlutil.h (include Streams.h) |
| Bibliothek| Strmbase.lib (Einzelhandels-Builds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaPosition-Klasse**](cmediaposition.md)
</dt> </dl>

 

 




