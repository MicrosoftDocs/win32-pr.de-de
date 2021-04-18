---
description: Die OnConnect-Methode stellt einen IUnknown-Zeiger auf das-Objekt bereit, das der Eigenschaften Seite zugeordnet ist.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: Cbasepropertypage. OnConnect-Methode (cprop. h)
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
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365654"
---
# <a name="cbasepropertypageonconnect-method"></a>Cbasepropertypage. OnConnect-Methode

Die- `OnConnect` Methode stellt einen **IUnknown** -Zeiger auf das-Objekt bereit, das der Eigenschaften Seite zugeordnet ist.

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

Ein Zeiger auf die **IUnknown** -Schnittstelle des Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Basisklassen Implementierung gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cbasepropertypage:: abtobjects**](cbasepropertypage-setobjects.md) -Methode ruft die- `OnConnect` Methode auf. Überschreiben Sie diese Methode, um einen Zeiger auf das von *punknown* angegebene Objekt zu speichern. Sie können entweder den *punknown* -Zeiger selbst speichern oder diesen Zeiger für andere Schnittstellen Abfragen. Wenn Sie den *punknown* -Zeiger speichern, wird vor der Rückgabe von " **adressf** " aufgerufen `OnConnect` .

Verwenden Sie in der [**cbasepropertypage:: onaktivierungs**](cbasepropertypage-onactivate.md) -Methode den gespeicherten Zeiger (oder Zeiger), um die Anfangswerte für die Dialog Eigenschaften abzurufen. Wenden Sie in der [**cbasepropertypage:: onapplychanges**](cbasepropertypage-onapplychanges.md) -Methode alle Änderungen auf das-Objekt zurück. Geben Sie alle Zeiger in der [**cbasepropertypage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) -Methode frei.

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
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




