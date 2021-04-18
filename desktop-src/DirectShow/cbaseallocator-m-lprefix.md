---
description: Präfix jedes Puffers in Bytes.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Cbasezucator:: m_lPrefix Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352884"
---
# <a name="cbaseallocatorm_lprefix-member"></a>Cbasezucator:: m \_ lprefix-Member

Präfix jedes Puffers in Bytes. Wenn der Wert ungleich 0 (null) ist, wird jedem Puffer Zeiger, der von der [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode zurückgegeben wird, ein Block von Bytes der Größe *m \_ lprefix* vorangestellt. Dieser Speicherblock wird als *Präfix* bezeichnet. Die Member-Variable [**cbasezucator:: m \_ LSIZE**](cbaseallocator-m-lsize.md) enthält nicht den Präfix Wert.

## <a name="syntax"></a>Syntax


```C++
long m_lPrefix;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasezucator-Klasse**](cbaseallocator.md)
</dt> </dl>

 

 




