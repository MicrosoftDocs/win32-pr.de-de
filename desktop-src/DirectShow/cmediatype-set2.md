---
description: Die Set-Methode legt den Medientyp von einem anderen Medientyp fest.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: CMediaType.Set-Methode (Mtype.h) – mtype [ref]-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 350e88cefa7c0f5f6946218d220fcad4a118cf53e203a68eeb9f75c0d0eace1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156063"
---
# <a name="cmediatypeset-method-mtypeh"></a>CMediaType.Set-Methode (Mtype.h)

Die `Set` -Methode legt den Medientyp von einem anderen Medientyp fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mtype* \[ Ref\]
</dt> <dd>

Verweis auf eine [**AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E \_ OUTOFMEMORY zurück.

## <a name="remarks"></a>Hinweise

Diese Methode kopiert den gesamten Medientyp aus *mtype*.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Mtype.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




