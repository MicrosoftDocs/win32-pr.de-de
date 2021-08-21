---
description: 'CMediaEvent.GetTypeInfo-Methode: Ruft ein Typinformationsobjekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.'
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: CMediaEvent.GetTypeInfo-Methode (Ctlutil.h)
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
ms.openlocfilehash: 3ef3f84cce1bad88b0f1103be3584ff350afac0fd7047b5a75a5fb473a4bedcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156988"
---
# <a name="cmediaeventgettypeinfo-method"></a>CMediaEvent.GetTypeInfo-Methode

Ruft ein Typinformationsobjekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.

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

Geben Sie informationen ein, die zurückgegeben werden sollen. Übergeben Sie 0 (null), um Typinformationen für die **IDispatch-Implementierung** abzurufen.

</dd> <dt>

*lcid* 
</dt> <dd>

Gebietsschema-ID für die Typinformationen. Für Klassen, die lokalisierte Membernamen unterstützen, kann ein Objekt möglicherweise unterschiedliche Typinformationen für verschiedene Sprachen zurückgeben. Für Klassen, die lokalisierte Membernamen nicht unterstützen, kann dieser Parameter ignoriert werden.

</dd> <dt>

*pptinfo* 
</dt> <dd>

Adresse eines Zeigers auf das angeforderte Typinformationsobjekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen E \_ POINTER zurück, wenn *pptinfo* ungültig ist. Gibt TYPE \_ E \_ ELEMENTNOTFOUND zurück, wenn *itinfo* nicht 0 (null) ist. Gibt S \_ OK zurück, wenn erfolgreich ist. Andernfalls gibt ein **HRESULT** aus einem der Aufrufe zurück, um den Typ abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMediaEvent-Klasse**](cmediaevent.md)
</dt> </dl>

 

 




