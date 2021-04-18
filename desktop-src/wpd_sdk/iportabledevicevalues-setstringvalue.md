---
description: Die SetStringValue-Methode fügt einen neuen Zeichen folgen Wert (Type VT \_ LPWSTR) hinzu oder überschreibt eine vorhandene.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'Iportabledevicevalues:: SetStringValue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366017"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a>Iportabledevicevalues:: SetStringValue-Methode

Die **SetStringValue** -Methode fügt einen neuen Zeichen folgen Wert (Type VT \_ LPWSTR) hinzu oder überschreibt eine vorhandene.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Ein **LPCWSTR** , der den neuen Wert angibt. Die Zeichenfolge wird kopiert, sodass der Aufrufer den für diesen Wert zugeordneten Arbeitsspeicher nach dem Aufrufen dieser Methode freigeben kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Angeben von Client Informationen](specifying-client-information.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hinzufügen einer Ressource zu einem Objekt](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Iportablede vicevalues:: GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[Festlegen von Eigenschaften für ein einzelnes Objekt](setting-properties-for-a-single-object.md)
</dt> <dt>

[Festlegen von Eigenschaften für mehrere Objekte](setting-properties-for-multiple-objects.md)
</dt> <dt>

[Angeben von Client Informationen](specifying-client-information.md)
</dt> <dt>

[Schreiben von Content-Object-Eigenschaften](writing-content-object-properties.md)
</dt> </dl>

 

 




