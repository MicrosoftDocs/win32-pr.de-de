---
description: 'CRendererPosPassThru.GetMediaTime-Methode: Die GetMediaTime-Methode ruft die Zeitstempel im aktuellen Beispiel ab.'
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: CRendererPosPassThru.GetMediaTime-Methode (Ctlutil.h)
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
ms.openlocfilehash: 588c92faec6b68cfa51392d4df00567c4e881460
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085368"
---
# <a name="crendererpospassthrugetmediatime-method"></a>CRendererPosPassThru.GetMediaTime-Methode

Die `GetMediaTime` -Methode ruft die Zeitstempel für das aktuelle Beispiel ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStartTime* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit in Einheiten des aktuellen Zeitformats empfängt.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeitformats empfängt. Kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                  | Beschreibung                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Die Konvertierung in dieses Format wird nicht unterstützt.<br/> |
| <dl> <dt>**E \_ POINTER**</dt> </dl>    | **NULL-Zeigerargument.**<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**CPosPassThru::GetMediaTime-Methode.**](cpospassthru-getmediatime.md) Die Zeitstempelwerte werden in das aktuelle Zeitformat konvertiert, indem die [**CPosPassThru::ConvertTimeFormat-Methode**](cpospassthru-converttimeformat.md) aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




