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
ms.openlocfilehash: 0fd2601b9f53e8f79d9231dd34054932bec4e671
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095438"
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

## <a name="remarks"></a>Bemerkungen

Die Basisklasse ändert den im *phr-Parameter* übergebenen **HRESULT-Wert** nicht.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




