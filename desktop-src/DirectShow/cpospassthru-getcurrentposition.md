---
description: Die GetCurrentPosition-Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die IMediaSeeking::GetCurrentPosition-Methode.
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: CPosPassThru.GetCurrentPosition-Methode (Ctlutil.h)
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
ms.openlocfilehash: a43477d019639b4e1de5c2aa40f18c99f7b902498c671f8106d5832c43b11584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084160"
---
# <a name="cpospassthrugetcurrentposition-method"></a>CPosPassThru.GetCurrentPosition-Methode

Die `GetCurrentPosition` -Methode ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab. Diese Methode implementiert die [**IMediaSeeking::GetCurrentPosition-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCurrent* 
</dt> <dd>

Zeiger auf eine Variable, die die aktuelle Position in Einheiten des aktuellen Zeitformats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                               | Beschreibung                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Die -Methode wird nicht unterstützt.<br/>   |
| <dl> <dt>**E \_ POINTER**</dt> </dl> | **NULL-Zeigerargument.**<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**CPosPassThru::GetMediaTime-Methode**](cpospassthru-getmediatime.md) auf, um die neueste Position abzurufen. Wenn **GetMediaTime** fehlschlägt, ruft die -Methode **IMediaSeeking::GetCurrentPosition** auf dem verbundenen Pin auf.

Die **GetMediaTime-Methode** schlägt in der Basisklasse standardmäßig fehl. Wenn Ihr Filter die aktuelle Position zwischenspeichert, überschreiben **Sie GetMediaTime,** um den zwischengespeicherten Wert zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




