---
description: 'Die QueryInternalConnections-Methode ruft die Pins ab, die intern mit dieser Pin (innerhalb des Filters) verbunden sind. Diese Methode implementiert die IPin:: QueryInternalConnections-Methode.'
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: Cbasepin. QueryInternalConnections-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356490"
---
# <a name="cbasepinqueryinternalconnections-method"></a>Cbasepin. QueryInternalConnections-Methode

Die- `QueryInternalConnections` Methode ruft die Pins ab, die intern mit dieser Pin (innerhalb des Filters) verbunden sind. Diese Methode implementiert die [**IPin:: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Appin* 
</dt> <dd>

Adresse eines Arrays von [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Zeigern.

</dd> <dt>

*npin* 
</dt> <dd>

Gibt bei Eingabe die Größe des Arrays an. Wenn die Methode zurückgibt, wird der Wert auf die Anzahl der im Array zurückgegebenen Zeiger festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                               | Beschreibung                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Unzureichende Array Größe.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>                 |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>    | Fehler.<br/>                 |
| <dl> <dt>**E \_ notimpl**</dt> </dl> | Nicht implementiert.<br/>         |



 

## <a name="remarks"></a>Bemerkungen

Bei manchen Filtern entsprechen Eingabe Pins bestimmten Ausgabe Pins. Für jede Pin füllt diese Methode ein Array mit Zeigern auf die entsprechenden Pins. Wenn jede Eingabe-PIN Daten für jede Ausgabe-PIN bereitstellt, wird E \_ notimpl zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




