---
description: Kritischer Abschnitt, der den Blockierungs Zustand schützt.
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: 'Cdynamicoutputpin:: m_BlockStateLock Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d9175342218e8b82698fe9b89d15937d6913e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364704"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a>Cdynamicoutputpin:: m \_ blockstatus-Member

Kritischer Abschnitt, der den Blockierungs Zustand schützt.

## <a name="syntax"></a>Syntax


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a>Bemerkungen

Halten Sie diesen kritischen Abschnitt vor, bevor Sie eine der folgenden Element Variablen verwenden:

-   [**Cdynamicoutputpin:: m \_ blockstate**](cdynamicoutputpin-m-blockstate.md)
-   [**Cdynamicoutputpin:: m \_ dwblockcallerthreadid**](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [**Cdynamicoutputpin:: m \_ dwnumoutstandingoutputpinusers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [**Cdynamicoutputpin:: m \_ hnotifycallerpinblockedevent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




