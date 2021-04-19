---
description: 'Die getpreroll-Methode ruft die Menge der Daten ab, die vor der Startposition in die Warteschlange eingereiht werden. Diese Methode implementiert die imediaseeking:: getpreroll-Methode.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Cpospassthru. getpreroll-Methode (ctlutil. h)
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
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369134"
---
# <a name="cpospassthrugetpreroll-method"></a>Cpospassthru. getpreroll-Methode

Die- `GetPreroll` Methode ruft die Menge der Daten ab, die vor der Startposition in die Warteschlange eingereiht werden. Diese Methode implementiert die [**imediaseeking:: getpreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pllpreroll* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die vorab Zeit in Einheiten des aktuellen Zeit Formats empfängt.

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

 

 




