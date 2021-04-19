---
description: 'Die converttimeformat-Methode konvertiert von einem Zeitformat in ein anderes. Diese Methode implementiert die imediaseeking:: converttimeformat-Methode.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Cpospassthru. converttimeformat-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bcce3e24c46e3e59c6bad6b4fbd60b139806de73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367663"
---
# <a name="cpospassthruconverttimeformat-method"></a>Cpospassthru. converttimeformat-Methode

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

Ein Zeiger auf die Zeitformat-GUID des Ziel Formats. Wenn der Wert **null** ist, wird das aktuelle Format verwendet.

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

Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> <dt>

[**Zeit Format-GUIDs**](time-format-guids.md)
</dt> </dl>

 

 




