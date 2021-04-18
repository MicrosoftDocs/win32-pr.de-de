---
description: Die isusingtimeformat-Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Csourceseeking. isusingtimeformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354644"
---
# <a name="csourceseekingisusingtimeformat-method"></a>Csourceseeking. isusingtimeformat-Methode

Die- `IsUsingTimeFormat` Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pformat* 
</dt> <dd>

Zeiger auf eine Zeitformat-GUID. Siehe [**Zeit Format-GUIDs**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                               | Beschreibung                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Das angegebene Format ist nicht das aktuelle Format.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Das angegebene Format ist das aktuelle Format.<br/>     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeigerargument.<br/>                      |



 

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

 

 




