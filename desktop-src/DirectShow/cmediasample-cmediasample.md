---
description: 'CMediaSample.CMediaSample-Konstruktor : Konstruktormethode.'
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: CMediaSample.CMediaSample-Konstruktor (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5baa5b791078eaf292b8da89fe50adaf7de9172185f8e6cab8745781030f401f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634690"
---
# <a name="cmediasamplecmediasample-constructor"></a>CMediaSample.CMediaSample-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*pAllocator* 
</dt> <dd>

Zeiger auf das [**CBaseAllocator-Objekt,**](cbaseallocator.md) das dieses Beispiel erstellt hat.

</dd> <dt>

*Phr* 
</dt> <dd>

Ignoriert.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Zeiger auf einen vom Aufrufer zugeordneten Speicherpuffer der *Größe*.

</dd> <dt>

*length* 
</dt> <dd>

Länge des Speicherpuffers.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Basisklasse ändert den **im phr-Parameter** übergebenen *HRESULT-Wert* nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




