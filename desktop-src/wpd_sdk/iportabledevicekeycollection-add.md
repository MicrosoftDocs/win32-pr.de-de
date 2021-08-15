---
description: Die Add-Methode fügt der Auflistung einen Eigenschaftsschlüssel hinzu.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: IPortableDeviceKeyCollection::Add-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 6aa28a7a8a6439f27a095033d35e8b066c1488af13d1ade921f16c4143843adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194720"
---
# <a name="iportabledevicekeycollectionadd-method"></a>IPortableDeviceKeyCollection::Add-Methode

Die **Add-Methode** fügt der Auflistung einen Eigenschaftsschlüssel hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY,** der der Auflistung hinzugefügt werden soll. Diese Methode kopiert den Schlüssel in die Auflistung, sodass Sie die lokale Variable nach dem Aufruf dieser Methode wieder frei geben können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                   | Beschreibung                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Die Methode wurde erfolgreich ausgeführt.<br/>                                                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um den Schlüssel zur Auflistung hinzuzufügen.<br/> |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Abrufen von Eigenschaften für ein einzelnes Objekt.](retrieving-properties-for-a-single-object.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[Abrufen von Inhaltsobjekteigenschaften](retrieving-content-object-properties.md)
</dt> <dt>

[Abrufen von Eigenschaften für ein einzelnes Objekt](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[Abrufen der von einem Gerät unterstützten Renderingfunktionen](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




