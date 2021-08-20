---
description: Windows Portable Devices (WPD) unterstützt die folgenden Eigenschaften von Befehlsparametern.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Befehlsparameter (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e5c58652c27d62e2954e86b9170e2f0a2d4ae4021743ced769adbf46a1f082b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431057"
---
# <a name="command-parameters"></a>Befehlsparameter

Windows Portable Devices (WPD) unterstützt die folgenden Eigenschaften von Befehlsparametern.




| **Eigenschaft**                                            | **VarType**     | **Beschreibung**                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFT \_ – ALLGEMEINE \_ \_ CLIENTINFORMATIONEN**          | **VT \_ UNKNOWN** | Eine [**IPortableDeviceValues-Schnittstelle,**](iportabledevicevalues.md) die der Treiber zum Identifizieren des Clients verwendet.                                                             |
| **\_WPD-EIGENSCHAFT: \_ ALLGEMEINE \_ \_ CLIENTINFORMATIONSKONTEXTE \_** | **VT \_ LPWSTR**  | Ein vom Treiber angegebener Kontext, der einen Client für alle nachfolgenden Vorgänge identifiziert.                                                                                          |
| **\_WPD-EIGENSCHAFT \_ ALLGEMEINE \_ \_ BEFEHLSKATEGORIE**            | **VT \_ CLSID**   | Der **GUID-Teil** des **PROPERTYKEY-Werts** des Befehls.                                                                                                            |
| **\_WPD-EIGENSCHAFT \_ : ALLGEMEINE \_ BEFEHLS-ID \_**                  | **VT \_ UI4**     | Der PiD-Teil (Persistent Unique ID) des **PROPERTYKEY-Werts** des Befehls.                                                                                          |
| **\_WPD-EIGENSCHAFT \_ COMMON COMMAND \_ \_ TARGET**              | **VT \_ LPWSTR**  | Der Zielobjektbezeichner.                                                                                                                                                |
| **\_WPD-EIGENSCHAFT \_ COMMON DRIVER \_ ERROR \_ \_ CODE**          | **VT \_ UI4**     | Ein treiberspezifischer Fehlercode, der von einem WPD-Treiber zurückgegeben wird.                                                                                                                       |
| **\_WPD-EIGENSCHAFT \_ COMMON \_ HRESULT**                      | **\_VT-FEHLER**   | Der **HRESULT-Wert,** der von einem WPD-Treiber für einen bestimmten Vorgang zurückgegeben wird.                                                                                                   |
| **\_WPD-EIGENSCHAFT \_ : ALLGEMEINE \_ \_ OBJEKT-IDs**                  | **VT \_ UNKNOWN** | Eine [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) des Variantentyps **VT \_ LPWSTR,** die eine Liste von Objektbezeichnern enthält. |
| **\_WPD-EIGENSCHAFT \_ COMMON PERSISTENT \_ UNIQUE \_ \_ IDS**      | **VT \_ UNKNOWN** | Eine [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) des Variantentyps **VT \_ LPWSTR,** die eine Liste von PIDs enthält.               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften und Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




