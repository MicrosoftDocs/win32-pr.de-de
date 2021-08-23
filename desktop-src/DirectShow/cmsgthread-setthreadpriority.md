---
description: Verwendet die Microsoft Win32 SetThreadPriority-Funktion, um die Priorität des Threads auf einen neuen Wert festzulegen.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: CMsgThread.SetThreadPriority-Methode (Msgthrd.h)
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
ms.openlocfilehash: ce293f32f765a89451ecf07b4532afc5fc4a7a132287d5b09b54962f93135215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585670"
---
# <a name="cmsgthreadsetthreadpriority-method"></a>CMsgThread.SetThreadPriority-Methode

Verwendet die Microsoft Win32 **SetThreadPriority-Funktion,** um die Priorität des Threads auf einen neuen Wert festzulegen.

## <a name="syntax"></a>Syntax


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nPriority* 
</dt> <dd>

Priorität des Threads.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                              | Beschreibung                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>TRUE!</dt> </dl>  | Die Priorität wurde erfolgreich festgelegt.<br/> |
| <dl> <dt>FALSE!</dt> </dl> | Die Priorität wurde nicht festgelegt.<br/>          |



 

## <a name="remarks"></a>Hinweise

Der Client und der Arbeitsthread können diese Memberfunktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMsgThread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




