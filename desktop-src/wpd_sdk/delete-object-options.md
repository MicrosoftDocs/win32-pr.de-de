---
description: Der \_ \_ Enumerationstyp "Objekt Optionen löschen" beschreibt Optionen, die beim Löschen eines Objekts von einem Gerät unterstützt werden.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: DELETE_OBJECT_OPTIONS-Enumeration (portabledevice. h)
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
ms.openlocfilehash: 3a1fb8ce9a443c7cc93019804094dca84a635c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368567"
---
# <a name="delete_object_options-enumeration"></a>\_Objekt \_ Optionen-Enumeration löschen

Der Enumerationstyp " **\_ Objekt \_ Optionen löschen** " beschreibt Optionen, die beim Löschen eines Objekts von einem Gerät unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**Portable \_ Geräte \_ Delete \_ keine \_ Rekursion**
</dt> <dd>

Löschen Sie das Objekt nur, und schlagen Sie fehl, wenn es untergeordnete Elemente

</dd> <dt>

<span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_Löschen von portablen Geräten \_ \_ mit \_ Rekursion**
</dt> <dd>

Löschen Sie das-Objekt und alle zugehörigen untergeordneten Elemente.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Anwendung kann die Lösch Optionen abrufen, die das Gerät unterstützt, indem [**iportabledevicecapabili:: getcommandoptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) für den Befehl **WPD \_ Command \_ Object \_ Management \_ Delete \_ Objects** aufgerufen wird. Der Wert für die Option " **\_ \_ \_ \_ rekursiver Löschvorgang \_ \_ unterstützt** ", der von dieser Methode in einem [**iportabledevicevaluescollection**](iportabledevicevaluescollection.md) -Objekt zurückgegeben wird, sollte untersucht werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen und Enumerationstypen**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




