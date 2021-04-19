---
description: Ein Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Cmediasample:: m_pAllocator Member (amfilter. h)'
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
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367555"
---
# <a name="cmediasamplem_pallocator-member"></a>Cmediasample:: m \_ pallocator-Member

Ein Zeiger auf die Zuweisung, die dieses Beispiel erstellt hat.

## <a name="syntax"></a>Syntax


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a>Bemerkungen

Obwohl das Beispiel einen Zeiger auf die Zuweisung beibehält, enthält es keinen Verweis Zähler. Stattdessen erhöht die Zuweisung ihren eigenen Verweis Zähler in der [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Methode und gibt sich selbst in der [**imemzuzucator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) -Methode frei. Dadurch wird sichergestellt, dass die Zuweisung verfügbar ist, solange das Beispiel von einem anderen Objekt verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediasample-Klasse**](cmediasample.md)
</dt> </dl>

 

 




