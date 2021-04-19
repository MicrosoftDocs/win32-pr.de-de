---
description: 'Die Clone-Methode erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. Diese Methode implementiert die ienummediatypes:: Clone-Methode.'
ms.assetid: 3b4eb29e-48fc-4f00-a5f3-597b9aa94ce1
title: Cenumschlag mediatypes. Clone-Methode (amfilter. h)
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
ms.openlocfilehash: 43f051bf90afa231d3b677045468f26d06d55150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367679"
---
# <a name="cenummediatypesclone-method"></a>Cenum mediatypes. Clone-Methode

Die- `Clone` Methode erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. Diese Methode implementiert die [**ienummediatypes:: Clone**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-clone) -Methode.

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

Adresse einer Variablen, die einen Zeiger auf die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle des neuen Enumerators empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                                | Beschreibung                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                 |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>              | Nicht genügend Arbeitsspeicher.<br/>                                                     |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>                  | **Null** -Zeigerargument.<br/>                                               |
| <dl> <dt>**VFW \_ E \_ Enum \_ nicht \_ \_ synchron**</dt> </dl> | Der Zustand der PIN wurde geändert und ist nun inkonsistent mit dem Enumerator.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cenum mediatypes-Klasse**](cenummediatypes.md)
</dt> </dl>

 

 




