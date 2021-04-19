---
description: Die widestringfromresource-Funktion lädt eine breit Zeichen-Zeichenfolge aus einer Ressourcen Datei mit dem angegebenen Ressourcen Bezeichner.
ms.assetid: c5fac767-20c4-4342-9d4d-e1b916854b95
title: Widestringfromresource-Funktion (wxutil. h)
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
ms.openlocfilehash: 9c7cbdccc76fc57e660109851ae5b8f141704d04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368587"
---
# <a name="widestringfromresource-function"></a>Widestringfromresource-Funktion

Die- `WideStringFromResource` Funktion lädt eine breit Zeichen-Zeichenfolge aus einer Ressourcen Datei mit dem angegebenen Ressourcen Bezeichner.

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

Ein Zeiger auf die Zeichenfolge, die " *iResourceID*" entspricht.

</dd> <dt>

*iResourceID* 
</dt> <dd>

Der Ressourcen Bezeichner der abzurufenden Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die gleiche Zeichenfolge wie *pbuffer* zurück. Wenn die Funktion nicht erfolgreich ist, wird eine NULL-Zeichenfolge zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Eigenschaften Seiten werden in der Regel über Ihre COM-Schnittstellen aufgerufen, die Zeichen folgen mit breit Zeichen verwenden, unabhängig davon, wie die Binärdatei erstellt wird. Diese Funktion ermöglicht es Ihnen, eine Ressourcen Zeichenfolge in eine Zeichenfolge mit breit Zeichen zu konvertieren. Die-Funktion konvertiert die Ressource nach dem Laden in eine Zeichenfolge mit breit Zeichen (wenn Sie noch nicht vorhanden ist).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hilfsfunktionen für Eigenschaften Seiten](property-page-helper-functions.md)
</dt> </dl>

 

 




