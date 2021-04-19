---
description: Die CheckRequest-Methode überprüft, ob eine Thread Anforderung vorhanden ist, ohne zu blockieren.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: Csourcestream. CheckRequest-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3100d449d2f29b2080541c5968cad6abc5643b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359406"
---
# <a name="csourcestreamcheckrequest-method"></a>Csourcestream. CheckRequest-Methode

Die- `CheckRequest` Methode überprüft, ob eine Thread Anforderung vorhanden ist, ohne zu blockieren.

## <a name="syntax"></a>Syntax


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCom* 
</dt> <dd>

Ein Zeiger auf eine Variable, die den Wert empfängt, der beim letzten Aufruf der Methode " [**camthread:: callworker**](camthread-callworker.md) " übermittelt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn eine ausstehende Anforderung vorhanden ist, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die Methode " [**camthread:: CheckRequest**](camthread-checkrequest.md) ", um eine Typüberprüfung durchzuführen. Die **csourcestream** -Klasse definiert den folgenden enumerierten Typ für den *pCom* -Parameter:


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




