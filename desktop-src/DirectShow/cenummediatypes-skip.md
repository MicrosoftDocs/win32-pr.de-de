---
description: Die Skip-Methode überspringt eine angegebene Anzahl von Medientypen. Diese Methode implementiert die IEnumMediaTypes::Skip-Methode.
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: CEnumMediaTypes.Skip-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a9930472b5c8a2873ca0a7f3280565bd41ac6b0aac7e1e33303464d3a2c1ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656445"
---
# <a name="cenummediatypesskip-method"></a>CEnumMediaTypes.Skip-Methode

Die `Skip` -Methode überspringt eine angegebene Anzahl von Medientypen. Diese Methode implementiert die [**IEnumMediaTypes::Skip-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip)

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Anzahl der zu überspringenden Medientypen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                | Beschreibung                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Übersprungen am Ende der Sequenz.<br/>                                    |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                 |
| <dl> <dt>**VFW \_ \_ E-ENUM \_ NICHT \_ \_ SYNCHRON**</dt> </dl> | Der Zustand des Pins hat sich geändert und ist jetzt inkonsistent mit dem Enumerator.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CEnumMediaTypes-Klasse**](cenummediatypes.md)
</dt> </dl>

 

 




