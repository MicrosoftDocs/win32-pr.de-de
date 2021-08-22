---
description: Gibt die Vererbungsbeziehung für einen Dienst an.
ms.assetid: e7f5314a-75e8-4f36-8e18-d614eda7a097
title: WPD_SERVICE_INHERITANCE_TYPES -Enumeration (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SERVICE_INHERITANCE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5a0e69986e7415a5a12eca7c450b0d7ff064c650d33c35997b9a166b01592c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444800"
---
# <a name="wpd_service_inheritance_types-enumeration"></a>WPD \_ SERVICE \_ INHERITANCE \_ TYPES-Enumeration

Der **WPD \_ SERVICE INHERITANCE \_ TYPES-Enumerationstyp \_** gibt die Vererbungsbeziehung für einen Dienst an.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_SERVICE_INHERITANCE_TYPES { 
  WPD_SERVICE_INHERITANCE_IMPLEMENTATION  = 0
} WPD_SERVICE_INHERITANCE_TYPES;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_SERVICE_INHERITANCE_IMPLEMENTATION"></span><span id="wpd_service_inheritance_implementation"></span>**\_ \_ WPD-DIENSTVERERBUNGSIMPLEMENTIERUNG \_**
</dt> <dd>

Der Dienst erbt durch Implementieren einer abstrakten Dienstdefinition.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IPortableDeviceServiceCapabilities::GetInheritedServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getinheritedservices)
</dt> </dl>

 

 




