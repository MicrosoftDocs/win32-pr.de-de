---
description: 'LPFNNewCOMObject-Funktionszeiger: Zeiger auf eine Funktion, die eine Instanz des -Objekts erstellt.'
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: LPFNNewCOMObject-Funktionszeiger (Combase.h)
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
ms.openlocfilehash: f3ea5bc172bc22f7aa9dce1f348bba552520565f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116528"
---
# <a name="lpfnnewcomobject-function-pointer"></a>LPFNNewCOMObject-Funktionszeiger

Zeiger auf eine Funktion, die eine Instanz des -Objekts erstellt.

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

Zeiger auf die **IUnknown-Schnittstelle** des Objekts, das das neue Objekt aggregiert, sofern verfügbar. Dieser Zeiger kann NULL **sein.**

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Wenn der Konstruktor fehlschlägt, empfängt dieser Parameter einen Fehlercode.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf eine neue Instanz des -Objekts zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Combase.h (einschließlich Streams.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CFactoryTemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




