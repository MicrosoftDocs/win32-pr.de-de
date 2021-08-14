---
description: Für Windows 7 unterstützt Windows Portable Devices die folgenden Attribute für Ereignisse eines Gerätediensts. Diese Attribute werden von der IPortableDeviceServiceCapabilities::GetEventAttributes-Methode zurückgegeben.
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Ereignisattribute (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 9ee6fe335d5e3906a923dfe5c470142cdf36fb1e521c3498963e478369a9b251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193291"
---
# <a name="event-attributes-portabledeviceh"></a>Ereignisattribute (PortableDevice.h)

Für Windows 7 unterstützt Windows Portable Devices die folgenden Attribute für Ereignisse eines Gerätediensts. Diese Attribute werden von der [**IPortableDeviceServiceCapabilities::GetEventAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) zurückgegeben.




| attribute                             | VarType         | BESCHREIBUNG                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ WPD-EREIGNISATTRIBUTNAME \_**       | **VT \_ LPWSTR**  | Eine Zeichenfolge, die den skriptfreundlichen Namen des Ereignisses angibt. Gültige Zeichen sind alphanumerische \[ Zeichen a-zA-Z0-9 \] und ' \_ '. |
| **OPTIONEN FÜR \_ WPD-EREIGNISATTRIBUTE \_ \_**    | **VT \_ UNKNOWN** | Ein [**IPortableDeviceValues-Wert,**](iportabledevicevalues.md) der die Ereignisoptionen enthält.                               |
| **\_ \_ WPD-EREIGNISATTRIBUTPARAMETER \_** | **VT \_ UNKNOWN** | Eine [**IPortableDeviceKeyCollection,**](iportabledevicekeycollection.md) die die Ereignisparameter enthält.              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Eigenschaften und Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




