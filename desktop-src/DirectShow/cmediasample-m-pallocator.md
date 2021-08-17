---
description: Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: CMediaSample::m_pAllocator-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 646c6fb7f8236aca87b5aebd1d30fd67750d960da4445d45bf45d8b601320274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156542"
---
# <a name="cmediasamplem_pallocator-member"></a>CMediaSample::m \_ pAllocator-Member

Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.

## <a name="syntax"></a>Syntax


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a>Hinweise

Das Beispiel behält zwar einen Zeiger auf die Zuweisung bei, enthält jedoch keinen Verweiszähler. Stattdessen erhöht die Zuweisung ihren eigenen Verweiszähler in der [**IMemAllocator::GetBuffer-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) und gibt sich selbst in der [**IMemAllocator::ReleaseBuffer-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) frei. Dadurch wird sichergestellt, dass die Zuweisung verfügbar ist, solange das Beispiel von einem anderen Objekt verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaSample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




