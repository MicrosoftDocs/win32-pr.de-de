---
description: Die Unadvise-Methode entfernt eine Empfehlungsanforderung.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: CABSchedule.Unadvise-Methode (Dsschedule.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bc9b1c964d698e1c1323846c7a25a29f60c0cd71009fbb60f1a09a6757b50b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057600"
---
# <a name="camscheduleunadvise-method"></a>CABSchedule.Unadvise-Methode

Die `Unadvise` -Methode entfernt eine Empfehlungsanforderung.

## <a name="syntax"></a>Syntax


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwAdviseCookie* 
</dt> <dd>

Der Bezeichner der Advise-Anforderung, der von der [**METHODE CABSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                             | Beschreibung          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Nicht gefunden<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dsschedule.h (include Streams.h)</dt> </dl>                                                                                |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WEBCAMSchedule-Klasse**](camschedule.md)
</dt> </dl>

 

 




