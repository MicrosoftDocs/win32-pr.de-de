---
title: D2D1CreateFactory Factory-Funktion (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2D1. h)
description: Erstellt ein Factory-Objekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann. | D2D1CreateFactory Factory-Funktion (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2D1. h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- D2D1CreateFactory Factory-Funktion (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e6588ef79b234402742d473982910255f4230
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350651"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a>D2D1CreateFactory <Factory> (D2D1 \_ Factory- \_ Typ, D2D1 \_ Factory- \_ Optionen&, Factory \* \* )-Funktion

Erstellt ein Factory-Objekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Vorlagenparameter



| Parameter | BESCHREIBUNG                                                 |
|-----------|-------------------------------------------------------------|
| *Schen* | Der Typ des zu erstellenden [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) . |



 

## <a name="parameters"></a>Parameter



| Parameter        | BESCHREIBUNG                                                                     |
|------------------|---------------------------------------------------------------------------------|
| *factoryType*    | Das Threading Modell der Factory und der von ihr erstellten Ressourcen.                |
| *facrenyoptions* | Die Detailebene, die für die debugschicht bereitgestellt wird.                            |
| *Fabrik*        | Wenn diese Methode zurückgegeben wird, enthält Sie die Adresse eines Zeigers auf die neue Factory. |



 

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |
| Bibliothek<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

