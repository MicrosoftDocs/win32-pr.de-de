---
description: Die passnotify-Methode übergibt eine Qualitäts Steuerungs Meldung an das entsprechende-Objekt.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Cbasonputpin. passnotify-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358019"
---
# <a name="cbaseinputpinpassnotify-method"></a>Cbasonputpin. passnotify-Methode

Die `PassNotify` -Methode übergibt eine Qualitäts Steuerungs Meldung an das entsprechende-Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Q1* 
</dt> <dd>

[**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur, die die Qualitäts Steuerungs Meldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                       | Beschreibung                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Erfolg.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ nicht \_ gefunden**</dt> </dl> | Es konnte kein Objekt gefunden werden, um die Nachricht zu akzeptieren.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ruft diese Methode auf, wenn der Filter keine Qualitäts Steuerungs Meldungen verarbeitet. Diese Methode übergibt die Nachricht in der angegebenen Reihenfolge an eines der folgenden Objekte:

-   Ein externer Qualitäts Steuerungs Manager, wenn die [**iqualitycontrol:: setsink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) -Methode aufgerufen wurde.
-   Die upstreamausgabepin.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> <dt>

[Qualitäts Steuerungs Verwaltung](quality-control-management.md)
</dt> </dl>

 

 




