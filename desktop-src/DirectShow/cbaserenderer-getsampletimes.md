---
description: Die getsampletimes-Methode ruft die Zeitstempel aus einem Beispiel ab.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: Cbaserderderer. getsampletimes-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c389c2ea55ddb15c59fe30e03f392d68aa3b5ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364857"
---
# <a name="cbaserenderergetsampletimes-method"></a>Cbaserderderer. getsampletimes-Methode

Die- `GetSampleTimes` Methode ruft die Zeitstempel aus einem Beispiel ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> <dt>

*pstarttime* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Startzeit empfängt.

</dd> <dt>

*Zeit* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                                    | Beschreibung                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                           | Das Beispiel sollte sofort gerendert werden.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl>                        | Das Beispiel sollte basierend auf den Zeitstempeln für das Rendering geplant werden.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                         | Führen Sie dieses Beispiel nicht aus.<br/>                                              |
| <dl> <dt>**VFW \_ E \_ \_ Startzeit \_ nach \_ Ende**</dt> </dl> | Ungültiger Zeitstempel: die Endzeit liegt vor der Startzeit.<br/>            |



 

## <a name="remarks"></a>Bemerkungen

Der Filter ruft diese Methode auf, um zu bestimmen, wie eine Stichprobe behandelt werden soll. Wenn der Rückgabewert S \_ OK ist, rendert der Filter das Beispiel sofort. Wenn der Rückgabewert S \_ false ist, plant der Filter das Rendering basierend auf den Zeitstempeln für das Rendering. Wenn der Rückgabewert ein Fehlercode ist, lehnt der Filter das Beispiel ab.

Diese Methode gibt "S OK" zurück \_ , wenn das Beispiel keine Zeitstempel aufweist, oder wenn der Filter keine Referenzuhr hat. Andernfalls wird der Wert der [**cbaserenderer:: denddrawsamplenow**](cbaserenderer-shoulddrawsamplenow.md) -Methode zurückgegeben. In der Basisklasse gibt " **schulddrawsamplenow** " immer "false" zurück \_ . Die abgeleitete Klasse kann dieses Verhalten überschreiben. Wenn die abgeleitete Klasse z. b. die Verwaltung von Qualitäts Teuerung implementiert, gibt Sie möglicherweise zurück, wenn \_ ein Beispiel nicht gelöscht wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




