---
description: 'Die canseekforward-Methode bestimmt, ob für den Datenstrom ein Seeding durchgeführt werden kann. Diese Methode implementiert die imediaposition:: canseekforward-Methode.'
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Cpospassthru. canseekforward-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 701bfdff1d3a3a37dc0e3935aa82bfca2e01cfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360887"
---
# <a name="cpospassthrucanseekforward-method"></a>Cpospassthru. canseekforward-Methode

Die- `CanSeekForward` Methode bestimmt, ob für den Datenstrom ein Seeding durchgeführt werden kann. Diese Methode implementiert die [**imediaposition:: canseekforward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcanseekforward* 
</dt> <dd>

Ein Zeiger auf eine Variable, die den Wert oatrue empfängt, wenn der Filter eine Suche durchsuchen oder andernfalls oafalse.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




