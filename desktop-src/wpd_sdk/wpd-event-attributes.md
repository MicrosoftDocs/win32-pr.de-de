---
description: 'Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für Ereignisse eines Geräte Dienstanbieter. Diese Attribute werden von der iportabledeviceservicecapabili:: geteventattributormethode zurückgegeben.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Ereignis Attribute (portabledevice. h)
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
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373574"
---
# <a name="event-attributes-portabledeviceh"></a>Ereignis Attribute (portabledevice. h)

Für Windows 7 unterstützt tragbare Windows-Geräte die folgenden Attribute für Ereignisse eines Geräte Dienstanbieter. Diese Attribute werden von der [**iportabledeviceservicecapabili:: geteventattributormethode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) zurückgegeben.




| Attribut                             | VarType         | BESCHREIBUNG                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| **Name des WPD- \_ Ereignis \_ Attributs \_**       | **VT \_ LPWSTR**  | Eine Zeichenfolge, die den Skript freundlichen Namen des Ereignisses angibt. Gültige Zeichen sind alphanumerisch \[ a-Za-z0-9 \] und ' \_ '. |
| **Optionen für das WPD- \_ Ereignis \_ Attribut \_**    | **VT \_ unbekannt** | Ein [**iportabledevicevalues**](iportabledevicevalues.md) -Element, das die Ereignis Optionen enthält.                               |
| **Parameter für WPD- \_ Ereignis \_ Attribute \_** | **VT \_ unbekannt** | Eine [**iportabledevicekeycollection**](iportabledevicekeycollection.md) , die die Ereignis Parameter enthält.              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften und Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




