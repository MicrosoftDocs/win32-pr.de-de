---
description: Flag zum angeben, ob ein Decommit-Vorgang ausgeführt wird.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Cbasezucator:: m_bDecommitInProgress Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27aaf2766f67ebb77250522346cfe5c76acdf6d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357597"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a>Cbasezucator:: m \_ bdecommitinprogress-Member

Flag zum angeben, ob ein Decommit-Vorgang ausgeführt wird. Der Wert ist " **true** ", nachdem die Methode " [**cbasezucator::D ecommit**](cbaseallocator-decommit.md) " aufgerufen wurde, aber bevor alle Puffer freigegeben wurden. Wenn der Wert **true** lautet, schlägt die [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode fehl. Außerdem sollte die Zuweisung nicht selbst gelöscht werden, wenn der Wert **true** ist.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bDecommitInProgress;
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

 

 




