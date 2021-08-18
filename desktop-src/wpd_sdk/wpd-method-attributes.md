---
description: Für Windows 7 unterstützt Windows Portable Devices die folgenden Attribute für Methoden eines Gerätediensts. Diese Attribute werden von der IPortableDeviceServiceCapabilities::GetMethodAttributes-Methode zurückgegeben.
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Methodenattribute (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ac41b4e9c7273c953a9689ce8c3d9f44d32925aded5b36291c45895b872fa9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026337"
---
# <a name="method-attributes"></a>Methodenattribut

Für Windows 7 unterstützt Windows Portable Devices die folgenden Attribute für Methoden eines Gerätediensts. Diese Attribute werden von der [**IPortableDeviceServiceCapabilities::GetMethodAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) zurückgegeben.




| attribute                                      | VarType         | Beschreibung                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ WPD-METHODENATTRIBUTZUGRIFF \_**             | **VT \_ CLSID**   | Der erforderliche Methodenzugriff.                                                                                               |
| **ZUGEORDNETES FORMAT \_ DES WPD-METHODENATTRIBUTS \_ \_ \_** | **VT \_ CLSID**   | Das format, das der -Methode zugeordnet ist, oder **GUID \_ NULL,** wenn kein zugeordnetes Format verfügbar ist.                                |
| **\_ \_ WPD-METHODENATTRIBUTNAME \_**               | **VT \_ LPWSTR**  | Eine Zeichenfolge, die den skriptfreundlichen Namen der Methode angibt. Gültige Zeichen sind alphanumerische \[ a-zA-Z0-9 \] und ' \_ '. |
| **\_ \_ WPD-METHODENATTRIBUTPARAMETER \_**         | **VT \_ UNKNOWN** | Eine [**IPortableDeviceKeyCollection-Schnittstelle,**](iportabledevicekeycollection.md) die die Methodenparameter enthält.    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Eigenschaften und Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




