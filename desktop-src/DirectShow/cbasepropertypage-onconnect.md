---
description: Die OnConnect-Methode stellt einen IUnknown-Zeiger auf das Der Eigenschaftenseite zugeordnete Objekt zur Seite.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: CBasePropertyPage.OnConnect-Methode (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: edc5448a20320e9bf74da7511bf6ae9fb9d95facc9b7973bbcd688127b495fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056100"
---
# <a name="cbasepropertypageonconnect-method"></a>CBasePropertyPage.OnConnect-Methode

Die `OnConnect` -Methode stellt einen **IUnknown-Zeiger** auf das Der Eigenschaftenseite zugeordnete Objekt zur Seite.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pUnknown* 
</dt> <dd>

Zeiger auf die **IUnknown-Schnittstelle** des -Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Basisklassenimplementierung gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Die [**CBasePropertyPage::SetObjects-Methode**](cbasepropertypage-setobjects.md) ruft die `OnConnect` -Methode auf. Überschreiben Sie diese Methode, um einen Zeiger auf das von *pUnknown angegebene Objekt zu speichern.* Sie können entweder den *pUnknown-Zeiger* selbst speichern oder diesen Zeiger für andere Schnittstellen abfragen. Wenn Sie den *pUnknown-Zeiger* speichern, rufen Sie **AddRef auf, bevor** zurückgegeben `OnConnect` wird.

Verwenden Sie [**in der CBasePropertyPage::OnActivate-Methode**](cbasepropertypage-onactivate.md) den gespeicherten Zeiger (oder Zeiger), um Anfangswerte für die Dialogeigenschaften abzurufen. Wenden Sie [**in der CBasePropertyPage::OnApplyChanges-Methode**](cbasepropertypage-onapplychanges.md) alle Änderungen zurück auf das -Objekt an. Geben Sie alle Zeiger in der [**CBasePropertyPage::OnDisconnect-Methode**](cbasepropertypage-ondisconnect.md) frei.

## <a name="examples"></a>Beispiele


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




