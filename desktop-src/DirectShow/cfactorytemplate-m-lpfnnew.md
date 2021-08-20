---
description: 'CFactoryTemplate::m_lpfnNew Member : Zeiger auf eine Funktion, die eine Instanz des -Objekts erstellt.'
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: CFactoryTemplate::m_lpfnNew-Member (Combase.h)
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
ms.openlocfilehash: 5a08b0f1b3dc28b70e62866b58a952b12959f0a7f753d5e6b4c847489b52bfd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317720"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>CFactoryTemplate::m \_ lpfnNew-Member

Zeiger auf eine Funktion, die eine Instanz des -Objekts erstellt.

## <a name="syntax"></a>Syntax


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>Hinweise

Deklarieren Sie in Ihrer DLL eine statische Funktion, die einen Zeiger auf eine neue Instanz des -Objekts zurückgibt. Legen Sie in der Factoryvorlage die **Membervariable m \_ lpfnNew** auf die Adresse dieser statischen Funktion fest.

Der Funktionszeigertyp ist [**LPFNNewCOMObject.**](lpfnnewcomobject.md)

Das folgende Beispiel zeigt eine typische Funktion für **m \_ lpfnNew**:


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



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CFactoryTemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




