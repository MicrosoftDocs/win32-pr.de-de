---
description: Die GetSyncSource-Methode ruft die Referenzuhr ab, die das Objekt verwendet. Diese Methode implementiert die IMediaFilter::GetSyncSource-Methode.
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: CBaseMediaFilter.GetSyncSource-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03bceee63109dedbf3b2fa9a855ddbfb410014d48de613f95c7bbfb98d6b0894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658873"
---
# <a name="cbasemediafiltergetsyncsource-method"></a>CBaseMediaFilter.GetSyncSource-Methode

Die `GetSyncSource` -Methode ruft die Verweisuhr ab, die das -Objekt verwendet. Diese Methode implementiert die [**IMediaFilter::GetSyncSource-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pclock* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IReferenceClock-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) der Uhr empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E \_ POINTER zurück.

## <a name="remarks"></a>Hinweise

Wenn das Objekt keine Verweisuhr verwendet, *\* wird pClock* auf **NULL festgelegt.** Wenn die Methode zurückgibt und *\* pClock* nicht **NULL** ist, verfügt die **IReferenceClock-Schnittstelle** über eine ausstehende Verweisanzahl. Stellen Sie sicher, dass Sie sie veröffentlichen, wenn Sie fertig sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseMediaFilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




