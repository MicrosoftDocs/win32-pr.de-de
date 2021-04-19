---
description: 'Die StartAt-Methode informiert die PIN, wann mit der Übermittlung von Daten begonnen werden soll. Diese Methode implementiert die iamstreamcontrol:: StartAt-Methode.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Cbasestreamcontrol. StartAt-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370492"
---
# <a name="cbasestreamcontrolstartat-method"></a>Cbasestreamcontrol. StartAt-Methode

Die- `StartAt` Methode informiert den PIN, wann die Übermittlung von Daten beginnen soll. Diese Methode implementiert die [**iamstreamcontrol:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptstart* 
</dt> <dd>

Ein Zeiger auf einen [**Verweis \_ Zeitwert**](reference-time.md) , der angibt, wann die PIN mit der Übermittlung von Daten beginnen soll.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Gibt einen Wert an, der zusammen mit der Start Benachrichtigung gesendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Strauch. h" (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasestreamcontrol-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




