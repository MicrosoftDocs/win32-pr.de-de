---
description: Die GetIPortableDeviceKeyCollectionValue-Methode ruft einen IPortableDeviceKeyCollection-Wert (Typ VT UNKNOWN) ab, der durch \_ einen Schlüssel angegeben wird.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 13a7ccde6a7cf5a73c78cc382341f7d750d9032cbfd8d69bdcfd3e318eeccece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194101"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a>IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue-Methode

Die **GetIPortableDeviceKeyCollectionValue-Methode** ruft einen **IPortableDeviceKeyCollection-Wert** (Typ VT UNKNOWN) ab, der durch \_ einen Schlüssel angegeben wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
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

Zeiger auf den abgerufenen [**IPortableDeviceKeyCollection-Schnittstellenzeiger.**](iportabledevicekeycollection.md) Der Aufrufer ist für den Aufruf von **Release auf** der abgerufenen Schnittstelle verantwortlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                            | Beschreibung                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                 |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | Die durch key angegebene *Eigenschaft* ist keine **IPortableDeviceKeyCollection-Schnittstelle.**<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ FOUND)**</dt> </dl> | Die durch key angegebene *Eigenschaft* ist nicht in der Auflistung.<br/>                             |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Abrufen von unterstützten Dienstereignissen.](retrieving-supported-events.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[Abrufen unterstützter Dienstereignisse](retrieving-supported-events.md)
</dt> <dt>

[Abrufen unterstützter Dienstmethoden](retrieving-supported-methods.md)
</dt> </dl>

 

 




