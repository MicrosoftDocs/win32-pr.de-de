---
description: 'Die GetCurrentPosition-Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die imediaseeking:: GetCurrentPosition-Methode.'
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Cpospassthru. GetCurrentPosition-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5cdbd93edf7630499f6585fbbf6e34a70bed68c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373822"
---
# <a name="cpospassthrugetcurrentposition-method"></a>Cpospassthru. GetCurrentPosition-Methode

Die- `GetCurrentPosition` Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die [**imediaseeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcurrent* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeit Formats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                               | Beschreibung                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                   |
| <dl> <dt>**E \_ notimpl**</dt> </dl> | Die Methode wird nicht unterstützt.<br/>   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeigerargument.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**cpospassthru:: getmediatime**](cpospassthru-getmediatime.md) -Methode auf, um die aktuelle Position abzurufen. Wenn **getmediatime** fehlschlägt, ruft die Methode **imediaseeking:: GetCurrentPosition** für die verbundene PIN auf.

Die **getmediatime** -Methode schlägt standardmäßig in der Basisklasse fehl. Wenn der Filter die aktuelle Position zwischenspeichert, überschreiben Sie **getmediatime** , um den zwischengespeicherten Wert zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




