---
description: Die StartAt-Methode informiert den Pin, wann mit der Übermittlung von Daten begonnen werden soll. Diese Methode implementiert die IAMStreamControl::StartAt-Methode.
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: CBaseStreamControl.StartAt-Methode (Strmctl.h)
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
ms.openlocfilehash: b40570933e7eed054694b2da927d71e077b86941aea816ff2ca6de5c91372b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814110"
---
# <a name="cbasestreamcontrolstartat-method"></a>CBaseStreamControl.StartAt-Methode

Die `StartAt` -Methode informiert den Pin, wann mit der Übermittlung von Daten begonnen werden soll. Diese Methode implementiert die [**IAMStreamControl::StartAt-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat)

## <a name="syntax"></a>Syntax


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptStart* 
</dt> <dd>

Zeiger auf einen [**REFERENCE \_ TIME-Wert,**](reference-time.md) der angibt, wann der Pin mit der Übermittlung von Daten beginnen soll.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Gibt einen Wert an, der zusammen mit der Startbenachrichtigung gesendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Strmctl.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseStreamControl-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




