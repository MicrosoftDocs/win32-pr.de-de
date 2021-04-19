---
description: Ruft ein Type-Information-Objekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Cmediaevent. gettypeingefo-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e351d3b8b06bea4f6f9a1a160802972a8fa50f82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361462"
---
# <a name="cmediaeventgettypeinfo-method"></a>Cmediaevent. gettypeingefo-Methode

Ruft ein Type-Information-Objekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*itinfo* 
</dt> <dd>

Typinformationen, die zurückgegeben werden. Übergeben Sie NULL, um Typinformationen für die **IDispatch** -Implementierung abzurufen.

</dd> <dt>

*lcid* 
</dt> <dd>

Die Gebiets Schema-ID für die Typinformationen. Bei Klassen, die lokalisierte Elementnamen unterstützen, kann ein Objekt möglicherweise unterschiedliche Typinformationen für verschiedene Sprachen zurückgeben. Für Klassen, die keine lokalisierten Elementnamen unterstützen, kann dieser Parameter ignoriert werden.

</dd> <dt>

*pptinfo* 
</dt> <dd>

Adresse eines Zeigers auf das angeforderte Type-Information-Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen E-Zeiger zurück, \_ Wenn *pptinfo* ungültig ist. Gibt den Typ \_ E \_ elementnotfound zurück, wenn *itinfo* nicht 0 (null) ist. Gibt S \_ OK zurück, wenn erfolgreich ist. Andernfalls wird ein **HRESULT** von einem der Aufrufe zurückgegeben, um den Typ abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmediaevent-Klasse**](cmediaevent.md)
</dt> </dl>

 

 




