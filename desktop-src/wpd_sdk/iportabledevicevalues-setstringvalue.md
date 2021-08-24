---
description: Die SetStringValue-Methode fügt einen neuen Zeichenfolgenwert (Typ VT LPWSTR) hinzu oder überschreibt \_ einen vorhandenen.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: IPortableDeviceValues::SetStringValue-Methode (PortableDeviceTypes.h)
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
ms.openlocfilehash: 0c00195823d71a59e706af1c0a627670f583776140772c3b8634ac10d7d95919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806860"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a>IPortableDeviceValues::SetStringValue-Methode

Die **SetStringValue-Methode** fügt einen neuen Zeichenfolgenwert (Typ VT LPWSTR) hinzu oder überschreibt \_ einen vorhandenen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Key* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY-Objekt,** das das zu erstellende oder zu überschreibende Element angibt.

</dd> <dt>

*Wert* \[ In\]
</dt> <dd>

Ein **LPCWSTR,** der den neuen Wert angibt. Die Zeichenfolge wird kopiert, sodass der Aufrufer den für diesen Wert zugeordneten Arbeitsspeicher nach dem Aufruf dieser Methode freigibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Jeder vorhandene Schlüsselspeicher wird entsprechend freigegeben.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Angeben von Clientinformationen.](specifying-client-information.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Hinzufügen einer Ressource zu einem Objekt](adding-a-resource-to-an-object.md)
</dt> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[Festlegen von Eigenschaften für ein einzelnes Objekt](setting-properties-for-a-single-object.md)
</dt> <dt>

[Festlegen von Eigenschaften für mehrere Objekte](setting-properties-for-multiple-objects.md)
</dt> <dt>

[Angeben von Clientinformationen](specifying-client-information.md)
</dt> <dt>

[Schreiben von Inhaltsobjekteigenschaften](writing-content-object-properties.md)
</dt> </dl>

 

 




