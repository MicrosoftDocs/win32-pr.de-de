---
description: Ein Zeiger auf eine Funktion, die eine Instanz des-Objekts erstellt.
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Lpfnnewcomobject-Funktionszeiger (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 07c0f8ab961c872c9dc0f92d2fff519b94cd049e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367701"
---
# <a name="lpfnnewcomobject-function-pointer"></a>Lpfnnewcomobject-Funktionszeiger

Ein Zeiger auf eine Funktion, die eine Instanz des-Objekts erstellt.

## <a name="syntax"></a>Syntax


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pUnkOuter* 
</dt> <dd>

Ein Zeiger auf die **IUnknown** -Schnittstelle des Objekts, das das neue Objekt aggregiert, sofern vorhanden. Dieser Zeiger kann **null** sein.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert. Wenn der Konstruktor ausfällt, empfängt dieser Parameter einen Fehlercode.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine neue Instanz des-Objekts zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cfactorytemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




