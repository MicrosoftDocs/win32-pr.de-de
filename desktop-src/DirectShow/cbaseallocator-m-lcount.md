---
description: Anzahl der Puffer, die bereitgestellt werden sollen.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Cbasezucator:: m_lCount Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372139"
---
# <a name="cbaseallocatorm_lcount-member"></a>Cbasezucator:: m \_ lCount-Member

Anzahl der Puffer, die bereitgestellt werden sollen. Die [**cbasezucator:: SetProperties**](cbaseallocator-setproperties.md) -Methode legt diesen Wert fest. Die Puffer werden erst zugeordnet, wenn die [**cbasezucator:: Commit**](cbaseallocator-commit.md) -Methode aufgerufen wird. Die aktuelle Anzahl der zugeordneten Puffer wird von der Variablen [**cbasezucator:: m \_ lzugeordnete**](cbaseallocator-m-lallocated.md) Member angegeben.

## <a name="syntax"></a>Syntax


```C++
long m_lCount;
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

 

 




