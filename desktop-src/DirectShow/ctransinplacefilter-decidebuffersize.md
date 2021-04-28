---
description: 'CTransInPlaceFilter.DecideBufferSize-Methode: Die DecideBufferSize-Methode legt die Pufferanforderungen des Ausgabepins fest.'
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: CTransInPlaceFilter.DecideBufferSize-Methode (Transip.h)
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
ms.openlocfilehash: b3ffb3ec7b1ef59c6e7f3d49e39fbe69e8cc1c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094828"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a>CTransInPlaceFilter.DecideBufferSize-Methode

Die `DecideBufferSize` -Methode legt die Pufferanforderungen des Ausgabepins fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAlloc* 
</dt> <dd>

Zeiger auf das [**IMemAllocator-Objekt,**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) das vom Ausgabepin verwendet wird.

</dd> <dt>

*pProperties* 
</dt> <dd>

Zeiger auf die angeforderten Zuweisungseigenschaften für Anzahl, Größe und Ausrichtung, wie von der [**ALLOCATOR \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                            | Beschreibung        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Fehler<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn die **CTransInPlaceFilter-Klasse** eine Puffergröße für den Downstreamfilter bereitstellen muss. Wenn der **CTransInPlaceFilter-Filter** bereits upstream verbunden ist, verwendet er die Zuweisungseigenschaften für die Upstream-Pinverbindung. Andernfalls wird die Puffergröße als temporärer Platzhalterwert auf 1 Byte festgelegt. Wenn der Upstreamfilter eine Verbindung herstellt, wird die Downstreamzuweisung von der **CTransInPlaceFilter-Klasse** neu ausgehandelt. Weitere Informationen zum Pinverbindungsprozess in dieser Klasse finden Sie unter [**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransInPlaceFilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




