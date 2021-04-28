---
description: 'CFactoryTemplate::m_lpfnNew Member : Zeiger auf eine Funktion, die eine Instanz des -Objekts erstellt.'
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: CFactoryTemplate::m_lpfnNew Member (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee4ec8e1503d3b260e025d154624b2d7c09bb49b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095648"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>CFactoryTemplate::m \_ lpfnNew-Member

Zeiger auf eine Funktion, die eine Instanz des -Objekts erstellt.

## <a name="syntax"></a>Syntax


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>Bemerkungen

Deklarieren Sie in Ihrer DLL eine statische Funktion, die einen Zeiger auf eine neue Instanz des -Objekts zurückgibt. Legen Sie in der Factoryvorlage die **Membervariable m \_ lpfnNew** auf die Adresse dieser statischen Funktion fest.

Der Funktionszeigertyp ist [**LPFNNewCOMObject.**](lpfnnewcomobject.md)

Das folgende Beispiel zeigt eine typische Funktion für **m \_ lpfnNew:**


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CFactoryTemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




