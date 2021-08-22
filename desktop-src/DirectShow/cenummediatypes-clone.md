---
description: Die Clone-Methode erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. Diese Methode implementiert die IEnumMediaTypes::Clone-Methode.
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: CEnumMediaTypes.Clone-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c624ac933228c769248c2980a250a9f89e9ebdaf386aeff951e70ba966311586
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537305"
---
# <a name="cenummediatypesclone-method"></a>CEnumMediaTypes.Clone-Methode

Die `Clone` -Methode erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. Diese Methode implementiert die [**IEnumMediaTypes::Clone-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone)

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnum* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IEnumMediaTypes-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) des neuen Enumerators empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                | Beschreibung                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>              | Nicht genügend Arbeitsspeicher.<br/>                                                     |
| <dl> <dt>**E \_ POINTER**</dt> </dl>                  | **NULL-Zeigerargument.**<br/>                                               |
| <dl> <dt>**VFW \_ E \_ ENUM \_ OUT \_ OF \_ SYNC**</dt> </dl> | Der Zustand des Pins wurde geändert und ist nun mit dem Enumerator inkonsistent.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CEnumMediaTypes-Klasse**](cenummediatypes.md)
</dt> </dl>

 

 




