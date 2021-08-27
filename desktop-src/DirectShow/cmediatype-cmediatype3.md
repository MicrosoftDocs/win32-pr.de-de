---
description: Erfahren Sie mehr über die CMediaType.CMediaType-Konstruktormethode (Mtype.h). Diese Methode verwendet die Parameter "mtype" und "phr".
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: CMediaType.CMediaType-Konstruktor (Mtype.h) – mtype- und phr-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c399073794f025122e1cfade3f15b3a96784f28e171482e4dcfb7bcec6a8271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084480"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a>CMediaType.CMediaType-Konstruktor (Mtype.h) – mtype- und phr-Parameter

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mtype* \[ Ref\]
</dt> <dd>

Verweis auf eine [**AM \_ MEDIA \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Der Konstruktor kopiert den Medientyp in das neue Objekt, einschließlich des Formatblocks, sofern vorhanden.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen HRESULT-Wert empfängt. Dieser Parameter kann ein **NULL-Zeiger** sein. Andernfalls muss der Aufrufer den Wert auf S OK festlegen, \_ bevor der Konstruktor aufgerufen wird. Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Konstruktor ruft die [**CMediaType::InitMediaType-Methode**](cmediatype-initmediatype.md) auf, um den Medientyp zu initialisieren.

## <a name="requirements"></a>Requirements (Anforderungen)

| Anforderung                   | Wert                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Mtype.h (include Streams.h)                                                                                     |
| Bibliothek | Strmbase.lib (Verkaufsbuilds); Strmbasd.lib (Debugbuilds) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaType-Klasse**](cmediatype.md)
</dt> </dl>

 

 




