---
description: 'Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für die Methoden eines Geräte Dienstanbieter. Diese Attribute werden von der iportabledeviceservicecapabili:: getmethodattributes-Methode zurückgegeben.'
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Methoden Attribute (portabledevice. h)
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
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370044"
---
# <a name="method-attributes"></a>Methodenattribut

Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für die Methoden eines Geräte Dienstanbieter. Diese Attribute werden von der [**iportabledeviceservicecapabili:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) -Methode zurückgegeben.




| Attribut                                      | VarType         | BESCHREIBUNG                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| **Zugriff auf WPD- \_ Methoden \_ Attribut \_**             | **VT \_ CLSID**   | Der erforderliche Methoden Zugriff.                                                                                               |
| **mit dem WPD- \_ Methoden \_ Attribut \_ verknüpfte \_ Format** | **VT \_ CLSID**   | Das Format, das der Methode zugeordnet ist, oder **GUID \_ null** , wenn kein zugeordnetes Format vorhanden ist.                                |
| **\_ \_ Attribut \_ Name der WPD-Methode**               | **VT \_ LPWSTR**  | Eine Zeichenfolge, die den Skript freundlichen Namen der Methode angibt. Gültige Zeichen sind alphanumerisch \[ a-Za-z0-9 \] und ' \_ '. |
| **\_ \_ Attribut \_ Parameter für WPD-Methoden**         | **VT \_ unbekannt** | Eine [**iportabledevicekeycollection**](iportabledevicekeycollection.md) -Schnittstelle, die die Methoden Parameter enthält.    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften und Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




