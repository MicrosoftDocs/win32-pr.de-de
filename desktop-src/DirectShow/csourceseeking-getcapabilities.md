---
description: 'Die getfunktionalitäten-Methode ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die imediaseeking:: getfunktionalitäten-Methode.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Csourceseeking. getSources-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda23944fd039576bb5de74fbb7c32e375415670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354647"
---
# <a name="csourceseekinggetcapabilities-method"></a>Csourceseeking. getSources-Methode

Die- `GetCapabilities` Methode ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die [**imediaseeking:: getfunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) -Methode.

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

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeiger Wert<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Suchfunktionen werden von der Element Variablen [**csourceseeking:: m \_ dwseekingcaps**](csourceseeking-m-dwseekingcaps.md) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




