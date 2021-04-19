---
description: Die getmediatime-Methode ruft die Zeitstempel im aktuellen Beispiel ab.
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Crendererpospassthru. getmediatime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 628c0f0c65dad4e00dd259edbeee97fd8f6f13ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373859"
---
# <a name="crendererpospassthrugetmediatime-method"></a>Crendererpospassthru. getmediatime-Methode

Die- `GetMediaTime` Methode ruft die Zeitstempel im aktuellen Beispiel ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstarttime* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Startzeit in Einheiten des aktuellen Zeit Formats empfängt.

</dd> <dt>

*Zeit* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeit Formats empfängt. Kann **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                  | Beschreibung                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                                    |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Die Konvertierung in dieses Format wird nicht unterstützt.<br/> |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | **Null** -Zeigerargument.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cpospassthru:: getmediatime**](cpospassthru-getmediatime.md) -Methode. Die Zeitstempel Werte werden in das aktuelle Zeitformat konvertiert, indem die [**cpospassthru:: converttimeformat**](cpospassthru-converttimeformat.md) -Methode aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




