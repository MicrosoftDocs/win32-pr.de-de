---
description: 'Die Benachrichtigungs Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die iqualitycontrol:: Notify-Methode.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Ctransformoutputpin. Notify-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ace7e25f1413f6e17a4d19ef937732ea8c689a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371245"
---
# <a name="ctransformoutputpinnotify-method"></a>Ctransformoutputpin. Notify-Methode

Die- `Notify` Methode benachrichtigt die PIN, dass eine Qualitätsänderung angefordert wird. Diese Methode implementiert die [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pself* 
</dt> <dd>

Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Filters, der die Qualitäts Steuerungs Meldung übermittelt hat.

</dd> <dt>

*Q1* 
</dt> <dd>

[**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur, die die Qualitäts Steuerungs Meldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                       | Beschreibung                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ nicht \_ gefunden**</dt> </dl> | Es konnte kein Objekt gefunden werden, um die Nachricht zu akzeptieren.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**ctransformfilter:: alterquality**](ctransformfilter-alterquality.md) -Methode des Filters auf. Wenn der Filter die Qualitäts Meldung nicht verarbeitet, ruft diese Methode die [**cbaseinputpin::P assnotify**](cbaseinputpin-passnotify.md) -Methode für die Eingabe-PIN des Filters auf. Die **passnotify** -Methode übergibt den upstreamnachrichten-Upstreamdienst (oder an einen benutzerdefinierten Quality Manager, wenn eine installiert wurde).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




