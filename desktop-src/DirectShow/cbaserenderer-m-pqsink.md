---
description: Zeiger auf das Objekt, das Qualitätskontrollnachrichten empfängt.
ms.assetid: bf4fd84c-9522-4686-9fb1-17a2ce3e5a16
title: CBaseRenderer::m_pQSink-Member (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pQSink
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb365c0af23868f05c624144de239828ce7c1d6cabacd3bf774c59d566348ff5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502720"
---
# <a name="cbaserendererm_pqsink-member"></a>CBaseRenderer::m \_ pQSink-Member

Zeiger auf das Objekt, das Qualitätskontrollnachrichten empfängt.

## <a name="syntax"></a>Syntax


```C++
IQualityControl *m_pQSink;
```



## <a name="remarks"></a>Hinweise

Die Basisklasse implementiert keine Qualitätskontrolle. Diese Membervariable wird standardmäßig auf **NULL** gesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




