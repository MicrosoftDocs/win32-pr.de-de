---
description: Die decidebuffersize-Methode legt die Puffer Anforderungen der Ausgabe-PIN fest.
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Ctransinplacefilter. decidebuffersize-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373683"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a>Ctransinplacefilter. decidebuffersize-Methode

Die `DecideBufferSize` -Methode legt die Puffer Anforderungen der Ausgabe-PIN fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*palloc* 
</dt> <dd>

Zeiger auf das [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Objekt, das von der Ausgabe-PIN verwendet wird.

</dd> <dt>

*pProperties* 
</dt> <dd>

Zeiger auf die angeforderten Zuweisungs Eigenschaften für Anzahl, Größe und Ausrichtung, wie in der [**Zuweisungs \_ Eigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) Struktur angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                            | Beschreibung        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Fehler<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn die **ctransinplacefilter** -Klasse eine Puffergröße für den downstreamfilter bereitstellen muss. Wenn der **ctransinplacefilter** -Filter bereits mit Upstream verbunden ist, werden die zuordnereigenschaften in der Upstream-Pin-Verbindung verwendet. Andernfalls wird die Puffergröße als temporärer Platzhalter Wert auf 1 Byte festgelegt. Wenn der upstreamfilter eine Verbindung herstellt, wird die Downstream-Zuweisung von der **ctransinplacefilter** -Klasse erneut ausgehandelt. Weitere Informationen zum Pin-Verbindungsprozess in dieser Klasse finden Sie unter [**ctransinplacefilter-Klasse**](ctransinplacefilter.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplacefilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




