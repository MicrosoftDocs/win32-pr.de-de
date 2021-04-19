---
description: 'Die querypreferredformat-Methode ruft das bevorzugte Zeitformat des Objekts ab. Diese Methode implementiert die imediaseeking:: querypreferredformat-Methode.'
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: Csourceseeking. querypreferredformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8916e23756279dd30eaf177ef839944a4c68d61a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353010"
---
# <a name="csourceseekingquerypreferredformat-method"></a>Csourceseeking. querypreferredformat-Methode

Die `QueryPreferredFormat` -Methode ruft das bevorzugte Zeitformat des Objekts ab. Diese Methode implementiert die [**imediaseeking:: querypreferredformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pformat* 
</dt> <dd>

Ein Zeiger auf eine Variable, die eine Zeitformat-GUID empfängt. Siehe [**Zeit Format-GUIDs**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                               | Beschreibung                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg<br/>                |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeiger Wert<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das einzige von der Basisklasse unterstützte Zeitformat ist die Zeit \_ Format \_ Medien \_ Zeit (100-Nanosecond-Einheiten).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




