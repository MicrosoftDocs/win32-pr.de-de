---
description: Die Add-Methode fügt der Auflistung einen Eigenschafts Schlüssel hinzu.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'Iportabledevicekeycollection:: Add-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e43fea25a08969b2ae8169884d51ddc46f8c7136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370782"
---
# <a name="iportabledevicekeycollectionadd-method"></a>Iportabledevicekeycollection:: Add-Methode

Die **Add** -Methode fügt der Auflistung einen Eigenschafts Schlüssel hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Ein **refpropertykey** , der der Auflistung hinzugefügt werden soll. Diese Methode kopiert den Schlüssel in die Auflistung, sodass Sie die lokale Variable freigeben können, nachdem Sie diese Methode aufgerufen haben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                   | Beschreibung                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Methode wurde erfolgreich ausgeführt.<br/>                                                  |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um der Sammlung den Schlüssel hinzuzufügen.<br/> |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Abrufen von Eigenschaften für ein einzelnes Objekt](retrieving-properties-for-a-single-object.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[Abrufen von Content-Object-Eigenschaften](retrieving-content-object-properties.md)
</dt> <dt>

[Abrufen von Eigenschaften für ein einzelnes Objekt](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[Abrufen der von einem Gerät unterstützten Renderingfunktionen](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




