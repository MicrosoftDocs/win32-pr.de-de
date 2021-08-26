---
description: Die IsUsingTimeFormat-Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: CSourceSeeking.IsUsingTimeFormat-Methode (Ctlutil.h)
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
ms.openlocfilehash: b930746102bc43e3549b4565a7591f4ac5fee8cc6503d9fb6aadcbe1659a52f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054240"
---
# <a name="csourceseekingisusingtimeformat-method"></a>CSourceSeeking.IsUsingTimeFormat-Methode

Die `IsUsingTimeFormat` -Methode bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFormat* 
</dt> <dd>

Zeiger auf eine Zeitformat-GUID. Weitere Informationen [**finden Sie unter Zeitformat-GUIDs.**](time-format-guids.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle aufgeführten **HRESULT-Werte** zurück.



| Rückgabecode                                                                               | Beschreibung                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Das angegebene Format ist nicht das aktuelle Format.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Das angegebene Format ist das aktuelle Format.<br/>     |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> |  NULL-Zeigerargument.<br/>                      |



 

## <a name="remarks"></a>Hinweise

Das einzige von der Basisklasse unterstützte Zeitformat ist TIME FORMAT MEDIA TIME (Einheiten von \_ \_ \_ 100 Nanosekunden).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceSeeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




