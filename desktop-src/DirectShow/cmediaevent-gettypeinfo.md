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
ms.openlocfilehash: f93e3227051729f9d16e1f9ef8de464a14cca33b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095568"
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

Geben Sie die zurückzugebende Information ein. Übergeben Sie 0 (null), um Typinformationen für die **IDispatch-Implementierung** abzurufen.

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



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaEvent-Klasse**](cmediaevent.md)
</dt> </dl>

 

 




