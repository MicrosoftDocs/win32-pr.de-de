---
description: Die GetIPortableDevicePropVariantCollectionValue-Methode ruft einen durch einen Schlüssel angegebenen IPortableDevicePropVariantCollection-Wert (Typ VT \_ UNKNOWN) ab.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d0ca7f2350fee8ba5d7cea85eb19c874eb5893f86f0e17fa1b4f0e97087e7c34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055190"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a>IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue-Methode

Die **GetIPortableDevicePropVariantCollectionValue-Methode** ruft einen **IPortableDevicePropVariantCollection-Wert** (Typ VT UNKNOWN) ab, der durch einen \_ Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Key* \[ In\]
</dt> <dd>

Ein **REFPROPERTYKEY-Schlüssel,** der das abzurufende Element angibt.

</dd> <dt>

*ppValue* \[ out\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die abgerufene [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) empfängt. Der Aufrufer ist für den Aufruf von **Release auf** der abgerufenen Schnittstelle verantwortlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                         |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | Die durch key angegebene *Eigenschaft* ist keine **IPortableDevicePropVariantCollection-Schnittstelle.**<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ FOUND)**</dt> </dl> | Die durch key angegebene *Eigenschaft* ist nicht in der Auflistung.<br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




