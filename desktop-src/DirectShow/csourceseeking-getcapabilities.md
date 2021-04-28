---
description: 'CSourceSeeking.GetCapabilities-Methode: Die GetCapabilities-Methode ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die IMediaSeeking::GetCapabilities-Methode.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: CSourceSeeking.GetCapabilities-Methode (Ctlutil.h)
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
ms.openlocfilehash: f1f354381c4c99cf880c75cbbc4b13355e386030
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098778"
---
# <a name="csourceseekinggetcapabilities-method"></a>CSourceSeeking.GetCapabilities-Methode

Die `GetCapabilities` -Methode ruft alle Suchfunktionen des Streams ab. Diese Methode implementiert die [**IMediaSeeking::GetCapabilities-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Zeiger auf eine Variable, die eine bitweise Kombination von [**AM \_ SEEKING SEEKING \_ \_ CAPABILITIES-Flags**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> | **NULL-Zeigerwert**<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Suchfunktionen werden von der [**CSourceSeeking::m \_ dwSeekingCaps-Membervariablen**](csourceseeking-m-dwseekingcaps.md) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




