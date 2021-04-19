---
description: Konstruktormethode.
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Cmsgthread. cmsgthread-Konstruktor (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77d3a84e349ab370b6319cd973f6ba86d632366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370738"
---
# <a name="cmsgthreadcmsgthread-constructor"></a>Cmsgthread. cmsgthread-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMsgThread();
```



## <a name="parameters"></a>Parameter

Dieser Konstruktor weist keine Parameter auf.

## <a name="remarks"></a>Bemerkungen

Beim Konstruieren eines Nachrichten Thread Objekts wird der Thread nicht automatisch erstellt. Sie müssen die Member-Funktion [**cmsgthread:: foratethread**](cmsgthread-createthread.md) aufrufen, um den Thread zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmsgthread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




