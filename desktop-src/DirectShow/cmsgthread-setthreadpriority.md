---
description: Verwendet die Microsoft Win32-Funktion SetThreadPriority, um die Priorität des Threads auf einen neuen Wert festzulegen.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: Cmsgthread. SetThreadPriority-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370923"
---
# <a name="cmsgthreadsetthreadpriority-method"></a>Cmsgthread. SetThreadPriority-Methode

Verwendet die Microsoft Win32-Funktion **SetThreadPriority** , um die Priorität des Threads auf einen neuen Wert festzulegen.

## <a name="syntax"></a>Syntax


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*npriorität* 
</dt> <dd>

Priorität des Threads.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                              | Beschreibung                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>TRUE * * * *</dt> </dl>  | Die Priorität wurde erfolgreich festgelegt.<br/> |
| <dl> <dt>FALSE * * * *</dt> </dl> | Es wurde keine Priorität festgelegt.<br/>          |



 

## <a name="remarks"></a>Bemerkungen

Der Client und der Arbeits Thread können diese Member-Funktion abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmsgthread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




