---
description: Die WideStringFromResource-Funktion lädt eine Breitzeichenzeichenfolge aus einer Ressourcendatei mit dem angegebenen Ressourcenbezeichner.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: WideStringFromResource-Funktion (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WideStringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798f915536c491d32ccab7e7dbdc9b506d8b5df22b4459818472307e62356b71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071814"
---
# <a name="widestringfromresource-function"></a>WideStringFromResource-Funktion

Die `WideStringFromResource` Funktion lädt eine Breitzeichenzeichenfolge aus einer Ressourcendatei mit dem angegebenen Ressourcenbezeichner.

## <a name="syntax"></a>Syntax


```C++
WCHAR* WINAPI WideStringFromResource(
   pBuffer *pBuffer,
   int     iResourceID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pBuffer* 
</dt> <dd>

Zeiger auf die Zeichenfolge, die *iResourceID entspricht.*

</dd> <dt>

*iResourceID* 
</dt> <dd>

Ressourcenbezeichner der abzurufenden Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt dieselbe Zeichenfolge wie *pBuffer zurück.* Wenn die Funktion nicht erfolgreich ist, gibt eine NULL-Zeichenfolge zurück.

## <a name="remarks"></a>Hinweise

Eigenschaftenseiten werden in der Regel über ihre COM-Schnittstellen aufgerufen, die Breitzeichenzeichenfolgen verwenden, unabhängig davon, wie die Binärdatei erstellt wird. Mit dieser Funktion können Sie eine Ressourcenzeichenfolge in eine Breitzeichenzeichenfolge konvertieren. Die Funktion konvertiert die Ressource nach dem Laden in eine Breitzeichenzeichenfolge (sofern noch nicht vorhanden).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Hilfsfunktionen für Eigenschaftenseiten](property-page-helper-functions.md)
</dt> </dl>

 

 




