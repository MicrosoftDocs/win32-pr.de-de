---
description: Der \_ DELETE OBJECT \_ OPTIONS-Enumerationstyp beschreibt Optionen, die von einem Gerät beim Löschen eines Objekts unterstützt werden.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: DELETE_OBJECT_OPTIONS-Enumeration (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 018c47a383a4fcd95d25bd13b00628678c6fa4a71e608f82544429020ea3f2c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194877"
---
# <a name="delete_object_options-enumeration"></a>DELETE \_ OBJECT \_ OPTIONS-Enumeration

Der **DELETE \_ OBJECT OPTIONS-Enumerationstyp \_** beschreibt Optionen, die von einem Gerät beim Löschen eines Objekts unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**PORTABLES \_ GERÄT LÖSCHEN \_ KEINE \_ \_ REKURSION**
</dt> <dd>

Löschen Sie nur das Objekt, und schlagen Sie fehl, wenn es über untergeordnete Elemente verfügt.

</dd> <dt>

<span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**PORTABLES \_ LÖSCHEN VON GERÄTEN MIT \_ \_ \_ RECURSION**
</dt> <dd>

Löschen Sie das Objekt und alle untergeordneten Elemente.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Anwendung kann die vom Gerät unterstützten Löschoptionen abrufen, indem [**sie IPortableDeviceCapabilities::GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) für den **BEFEHL WPD COMMAND OBJECT MANAGEMENT \_ DELETE \_ \_ \_ \_ OBJECTS** aufruft. Es sollte den **WPD \_ OPTION OBJECT MANAGEMENT \_ \_ \_ RECURSIVE \_ DELETE \_ SUPPORTED-Optionswert** untersuchen, den diese Methode in einem [**IPortableDeviceValuesCollection-Objekt**](iportabledevicevaluescollection.md) zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




