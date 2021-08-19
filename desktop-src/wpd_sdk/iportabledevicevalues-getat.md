---
description: Die GetAt-Methode ruft einen Wert aus der Auflistung mithilfe des angegebenen nullbasierten Indexes ab.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: IPortableDeviceValues::GetAt-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4e234d0fe24eec947b388b5da798c55e7478ffa6bda69a9b9fe57c279af6d96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843023"
---
# <a name="iportabledevicevaluesgetat-method"></a>IPortableDeviceValues::GetAt-Methode

Die **GetAt-Methode** ruft einen Wert aus der Auflistung mithilfe des angegebenen nullbasierten Indexes ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Ein **DWORD,** das einen nullbasierten Index in der Auflistung angibt.

</dd> <dt>

*pKey* \[ in, out\]
</dt> <dd>

Ein optionaler **PROPERTYKEY-Zeiger,** der den Schlüssel des angegebenen Elements abruft.

</dd> <dt>

*pValue* \[ in, out\]
</dt> <dd>

Ein optionales **PROPVARIANT,** das den Wert des angegebenen Elements abruft. Der Aufrufer muss den Arbeitsspeicher freigeben, indem **er PropVariantClear** aufruft, wenn dies abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Es wurde eine ungültige Indexnummer angegeben.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn eine Eigenschaft einen Wert vom Typ VT \_ UNKNOWN angibt, ist die Eigenschaft eines der Windows Portable Devices ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) oder [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)). Von Windows Portable Devices können keine anderen Schnittstellen zurückgegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




