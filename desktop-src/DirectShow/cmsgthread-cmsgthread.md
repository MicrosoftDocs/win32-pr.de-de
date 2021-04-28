---
description: 'CMsgThread.CMsgThread-Konstruktor : Konstruktormethode.'
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: CMsgThread.CMsgThread-Konstruktor (Msgthrd.h)
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
ms.openlocfilehash: 08d76ebecd09d95b7ba0fca22b300c1e402f5302
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095368"
---
# <a name="cmsgthreadcmsgthread-constructor"></a>CMsgThread.CMsgThread-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CMsgThread();
```



## <a name="parameters"></a>Parameter

Dieser Konstruktor verfügt über keine Parameter.

## <a name="remarks"></a>Bemerkungen

Beim Erstellen eines Nachrichtenthreadobjekts wird der Thread nicht automatisch erstellt. Sie müssen die [**CMsgThread::CreateThread-Memberfunktion**](cmsgthread-createthread.md) aufrufen, um den Thread zu erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMsgThread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




