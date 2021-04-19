---
description: 'Der Bezeichner des Threads, der zuletzt die IPinFlowControl:: Block-Methode für diese Pin aufgerufen hat. Diese Element Variable ist nur gültig, wenn die PIN blockiert ist.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Cdynamicoutputpin:: m_dwBlockCallerThreadID Member (amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372751"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>Cdynamicoutputpin:: m \_ dwblockcallerthreadid-Member

Der Bezeichner des Threads, der zuletzt die [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) -Methode für diese Pin aufgerufen hat. Diese Element Variable ist nur gültig, wenn die PIN blockiert ist.

## <a name="syntax"></a>Syntax


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>Bemerkungen

Bevor Sie auf diese Variable zugreifen, halten Sie den kritischen Abschnitt [**cdynamicoutputpin:: m \_ blockstatus eLOCK**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




