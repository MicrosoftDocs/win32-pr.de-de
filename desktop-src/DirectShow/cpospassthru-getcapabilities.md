---
description: 'Die getfunktionalitäten-Methode ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die imediaseeking:: getfunktionalitäten-Methode.'
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: Cpospassthru. getfunktionalitäten-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f896adbc1015cb34e6f9063cb5ebf73e5cdb441c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358069"
---
# <a name="cpospassthrugetcapabilities-method"></a>Cpospassthru. getfunktionalitäten-Methode

Die **getfunktionalitäten** -Methode ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die [**imediaseeking:: getfunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfunktionen* 
</dt> <dd>

Ein Zeiger auf eine Variable, die eine bitweise Kombination von für Suchvorgänge [**\_ \_ suchbare \_**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) Flags empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




