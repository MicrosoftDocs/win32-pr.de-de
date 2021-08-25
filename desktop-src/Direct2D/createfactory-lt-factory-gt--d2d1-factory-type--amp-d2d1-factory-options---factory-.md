---
title: D2D1CreateFactory Factory -Funktion (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) (D2d1.h)
description: Erstellt ein Factoryobjekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann. | D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) -Funktion (D2d1.h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- D2D1CreateFactory Factory-Funktion (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Direct2D
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
ms.openlocfilehash: 34cbe566b139ebd873e8e9895aa21307113be9632b2045d40c099f52f49fc574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824690"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a>D2D1CreateFactory <Factory> (D2D1 \_ FACTORY \_ TYPE,D2D1 \_ FACTORY OPTIONS \_&,Factory \* \* ) -Funktion

Erstellt ein Factoryobjekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Vorlagenparameter



| Parameter | Beschreibung                                                 |
|-----------|-------------------------------------------------------------|
| *Fabrik* | Der Typ der [**zu erstellenden ID2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) |



 

## <a name="parameters"></a>Parameter



| Parameter        | Beschreibung                                                                     |
|------------------|---------------------------------------------------------------------------------|
| *factoryType*    | Das Threadingmodell der Factory und die von ihr erstellten Ressourcen.                |
| *factoryOptions* | Die Detailebene, die für die Debugebene bereitgestellt wird.                            |
| *Fabrik*        | Enthält nach der Rückkehr dieser Methode die Adresse eines Zeigers auf die neue Factory. |



 

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Windows Vista mit SP2 und Plattformupdate für Windows Vista-Desktop-Apps \[ \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate für Windows Server 2008-Desktop-Apps \[ \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 und Windows Runtime-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |
| Bibliothek<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

