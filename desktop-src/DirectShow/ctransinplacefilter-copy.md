---
description: Die Copy-Methode kopiert ein Medien Beispiel.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: Ctransinplacefilter. Copy-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3063427611cd3a5aae74fecf6be273c07fdb917c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370827"
---
# <a name="ctransinplacefiltercopy-method"></a>Ctransinplacefilter. Copy-Methode

Die- `Copy` Methode kopiert ein Medien Beispiel.

## <a name="syntax"></a>Syntax


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psource* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf die **imediasample** -Schnittstelle im neuen Beispiel zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft einen leeren Puffer von der Downstream-Zuweisung ab. Alle Beispiel Eigenschaften werden zusammen mit den eigentlichen Daten aus dem Beispiel aus *psource* in das neue Beispiel kopiert. Wenn der Filter zwei Zuweisungen verwendet, wird diese Methode aufgerufen, um Daten über Puffer hinweg zu kopieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransinplacefilter-Klasse**](ctransinplacefilter.md)
</dt> </dl>

 

 




