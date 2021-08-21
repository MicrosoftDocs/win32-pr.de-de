---
description: Die GetPreroll-Methode ruft die Datenmenge ab, die vor der Startposition in die Warteschlange gestellt wird. Diese Methode implementiert die IMediaSeeking::GetPreroll-Methode.
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: CPosPassThru.GetPreroll-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b34cd565d246f4401061834b21c005306633e72a6f24cc8367a222b5f3736c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954039"
---
# <a name="cpospassthrugetpreroll-method"></a>CPosPassThru.GetPreroll-Methode

Die `GetPreroll` -Methode ruft die Datenmenge ab, die vor der Startposition in die Warteschlange gestellt wird. Diese Methode implementiert die [**IMediaSeeking::GetPreroll-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pllPreroll* 
</dt> <dd>

Zeiger auf eine Variable, die die Vorabrollzeit in Einheiten des aktuellen Zeitformats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




