---
description: 'CMediaControl.GetTypeInfo-Methode: Ruft ein Typinformationsobjekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.'
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: CMediaControl.GetTypeInfo-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857dbdeee9a2add9ab77cae0ff97d69699d2dd2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099128"
---
# <a name="cmediacontrolgettypeinfo-method"></a>CMediaControl.GetTypeInfo-Methode

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

Geben Sie informationen ein, die sie zurückgeben. Übergeben Sie 0 (null), um Typinformationen für die **IDispatch-Implementierung** abzurufen.

</dd> <dt>

*lcid* 
</dt> <dd>

Die Locale ID für die Typinformationen. Für Klassen, die lokalisierte Membernamen unterstützen, kann ein Objekt möglicherweise unterschiedliche Typinformationen für verschiedene Sprachen zurückgeben. Für Klassen, die lokalisierte Membernamen nicht unterstützen, kann dieser Parameter ignoriert werden.

</dd> <dt>

*pptinfo* 
</dt> <dd>

Adresse eines Zeigers auf das angeforderte Typinformationsobjekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen \_ E-ZEIGER zurück, *wenn pptinfo* ungültig ist. Gibt TYPE \_ E \_ ELEMENTNOTFOUND zurück, *wenn itinfo* nicht 0 (null) ist. Gibt S \_ OK zurück, wenn erfolgreich ist. Andernfalls gibt ein **HRESULT aus** einem der Aufrufe zurück, um den Typ abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMediaControl-Klasse**](cmediacontrol.md)
</dt> </dl>

 

 




