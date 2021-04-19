---
description: Ein Zeiger auf eine Funktion, die eine Instanz des-Objekts erstellt.
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'Cfactoriytemplate:: m_lpfnNew Member (ComBase. h)'
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
ms.openlocfilehash: 2299f7a87f348ac8a5fa6c6d83b6a17fbf97ca28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359641"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>Cfactor ytemplate:: m \_ lpfnnew-Member

Ein Zeiger auf eine Funktion, die eine Instanz des-Objekts erstellt.

## <a name="syntax"></a>Syntax


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>Bemerkungen

Deklarieren Sie in der DLL eine statische Funktion, die einen Zeiger auf eine neue Instanz des-Objekts zurückgibt. Legen Sie in der Factory-Vorlage die **m \_ lpfnnew** -Member-Variable auf die Adresse dieser statischen Funktion fest.

Der Funktions Zeigertyp ist " [**lpfnnewcomobject**](lpfnnewcomobject.md)".

Das folgende Beispiel zeigt eine typische Funktion für **m \_ lpfnnew**:


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
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cfactorytemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




