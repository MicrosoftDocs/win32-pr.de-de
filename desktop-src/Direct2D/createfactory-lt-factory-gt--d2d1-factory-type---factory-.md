---
title: D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, Factory)-Funktion (D2D1. h)
description: Erstellt ein Factory-Objekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann. | D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, Factory)-Funktion (D2D1. h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- D2D1CreateFactory Factory-Funktion (D2D1_FACTORY_TYPE, Factory) Direct2D
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
ms.openlocfilehash: c03400cec8c838ba561a7eb504674e074d7b3199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106373477"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a>D2D1CreateFactory <Factory> (D2D1 \_ Factory \_ Type, Factory \* \* )-Funktion

Erstellt ein Factory-Objekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Vorlagenparameter



| Parameter | BESCHREIBUNG                                                 |
|-----------|-------------------------------------------------------------|
| *Schen* | Der Typ des zu erstellenden [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) . |



 

## <a name="parameters"></a>Parameter



| Parameter     | BESCHREIBUNG                                                                     |
|---------------|---------------------------------------------------------------------------------|
| *factoryType* | Das Threading Modell der Factory und der von ihr erstellten Ressourcen.                |
| *Fabrik*     | Wenn diese Methode zurückgegeben wird, enthält Sie die Adresse eines Zeigers auf die neue Factory. |



 

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |
| Bibliothek<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

