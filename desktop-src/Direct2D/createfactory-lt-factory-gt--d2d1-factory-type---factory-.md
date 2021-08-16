---
title: D2D1CreateFactory Factory -Funktion (D2D1_FACTORY_TYPE,Factory) (D2d1.h)
description: Erstellt ein Factoryobjekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann. | D2D1CreateFactory Factory -Funktion (D2D1_FACTORY_TYPE,Factory) (D2d1.h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Funktion Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af5635a6f996ea6cd3af2c3b3022efa054cd27605430c8230143980e00b9abbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826469"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a>D2D1CreateFactory <Factory> (D2D1 \_ FACTORY \_ TYPE,Factory \* \* ) -Funktion

Erstellt ein Factoryobjekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Vorlagenparameter



| Parameter | Beschreibung                                                 |
|-----------|-------------------------------------------------------------|
| *Fabrik* | Der Typ von [**ID2D1Factory,**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) der erstellt werden soll. |



 

## <a name="parameters"></a>Parameter



| Parameter     | Beschreibung                                                                     |
|---------------|---------------------------------------------------------------------------------|
| *factoryType* | Das Threadingmodell der Factory und die von ihr erstellten Ressourcen.                |
| *Fabrik*     | Diese Methode gibt die Adresse eines Zeigers auf die neue Factory zurück. |



 

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine Factory erstellt.


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Windows Vista mit SP2 und Plattformupdate für UWP-Apps für Windows \[ \| Vista-Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate für Windows Server \[ 2008-Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |
| Bibliothek<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

