---
description: 'Die canseekabwärts-Methode bestimmt, ob der Stream rückwärts Seeding durchgeführt werden kann. Diese Methode implementiert die imediaposition:: canseekabwärts-Methode.'
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Cpospassthru. canseekabwärts-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367583"
---
# <a name="cpospassthrucanseekbackward-method"></a>Cpospassthru. canseekabwärts-Methode

Die- `CanSeekBackward` Methode bestimmt, ob der Stream rückwärts Seeding durchgeführt werden kann. Diese Methode implementiert die [**imediaposition:: canseekabwärts**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcanseekabwärts* 
</dt> <dd>

Ein Zeiger auf eine Variable, die den Wert oatrue empfängt, wenn der Filter rückwärts suchen oder andernfalls oafalse.

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

 

 




