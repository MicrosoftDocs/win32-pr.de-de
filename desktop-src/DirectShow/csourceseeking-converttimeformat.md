---
description: 'Die converttimeformat-Methode konvertiert von einem Zeitformat in ein anderes. Diese Methode implementiert die imediaseeking:: converttimeformat-Methode.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Csourceseeking. converttimeformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3869ef5bc9656414ca5b465a04d04a4ca4be41e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354063"
---
# <a name="csourceseekingconverttimeformat-method"></a>Csourceseeking. converttimeformat-Methode

Die- `ConvertTimeFormat` Methode konvertiert von einem Zeitformat in ein anderes. Diese Methode implementiert die [**imediaseeking:: converttimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTARGET* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die konvertierte Zeit empfängt.

</dd> <dt>

*ptargetformat* 
</dt> <dd>

Zeiger auf die GUID des Ziel Formats. Wenn der Wert **null** ist, wird das aktuelle Format verwendet. Siehe [**Zeit Format-GUIDs**](time-format-guids.md).

</dd> <dt>

*Quelle* 
</dt> <dd>

Zeitwert, der konvertiert werden soll.

</dd> <dt>

*psourceformat* 
</dt> <dd>

Ein Zeiger auf die Zeitformat-GUID des zu konvertierenden Formats. Wenn der Wert **null** ist, wird das aktuelle Format verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                  | Beschreibung                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg<br/>                   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültiges Argument<br/>          |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | **Null** -Zeigerargument<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das einzige von der Basisklasse unterstützte Zeitformat ist die Zeit \_ Format \_ Medien \_ Zeit (100-Nanosecond-Einheiten). Diese Methode gibt E \_ invalidArg zurück, außer in dem trivialen Fall, in dem *ptargetformat* und *psourceformat* beide die Zeit \_ Format \_ Medien \_ Zeit angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourceseeking-Klasse**](csourceseeking.md)
</dt> </dl>

 

 




