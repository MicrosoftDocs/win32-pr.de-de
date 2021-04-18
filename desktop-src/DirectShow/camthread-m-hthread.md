---
description: Handle für den Thread.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'Camthread:: m_hThread Member (wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358796"
---
# <a name="camthreadm_hthread-member"></a>Camthread:: m- \_ hThread-Member

Handle für den Thread.

## <a name="syntax"></a>Syntax


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a>Bemerkungen

Diese Variable wird als **null** initialisiert. Die Methode " [**camthread:: Create**](camthread-create.md) " legt diese Variable auf das Thread Handle fest. Um zu ermitteln, ob der Thread vorhanden ist, müssen Sie die Methode " [**camthread:: threadexists**](camthread-threadexists.md) " aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




