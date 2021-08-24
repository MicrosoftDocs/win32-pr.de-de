---
description: Die Clone-Methode erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. Diese Methode implementiert die IEnumPins::Clone-Methode.
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: CEnumPins.Clone-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a0d14f0caf30f6037d53639ff54d2e21d6d0fb0eee5cfa493aba248e84d48e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688610"
---
# <a name="cenumpinsclone-method"></a>CEnumPins.Clone-Methode

Die `Clone` -Methode erstellt eine Kopie des Enumerators mit dem gleichen Enumerationszustand. Diese Methode implementiert die [**IEnumPins::Clone-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone)

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnum* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IEnumPins-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) des neuen Enumerators empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                | Beschreibung                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>              | Nicht genügend Arbeitsspeicher.<br/>                                                        |
| <dl> <dt>**E \_ POINTER**</dt> </dl>                  | **NULL-Zeigerargument.**<br/>                                                  |
| <dl> <dt>**VFW \_ E \_ ENUM \_ OUT \_ OF \_ SYNC**</dt> </dl> | Der Status des Filters hat sich geändert und ist nun mit dem Enumerator inkonsistent.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CEnumPins-Klasse**](cenumpins.md)
</dt> </dl>

 

 




