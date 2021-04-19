---
description: Tragbare Windows-Geräte unterstützen die folgenden Ressourcen Attribut Eigenschaften.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Eigenschaften des Ressourcen Attributs (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356052"
---
# <a name="resource-attribute-properties"></a>Eigenschaften des Ressourcen Attributs

Tragbare Windows-Geräte unterstützen die folgenden Ressourcen Attribut Eigenschaften.



| Eigenschaft                                    | VarType         | BESCHREIBUNG                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ressourcen Schlüssel für WPD- \_ Ressourcen \_ Attribut \_ \_** | **VT \_ unbekannt** | Dies ist eine [**iportabledevicekeycollection**](iportabledevicekeycollection.md) , die einen einzelnen Wert enthält. Dies ist der Schlüssel, der die Ressource identifiziert.                     |
| **WPD- \_ Ressourcen \_ Attribut \_ Format**        | **VT \_ CLSID**   | Ein GUID-Wert, der das Format der Ressource angibt. Eine Liste der Formate, die von tragbaren Windows-Geräten definiert werden, finden Sie unter [Objekt Formate](object-format-guids.md) . |
| **Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_**   | **VT \_ UI8**     | Die Gesamtgröße der Ressourcen Daten in Bytes.                                                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Diese Attribute werden von der [**iportabledeviceresources:: getresourceattributormethode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportabledeviceresources:: getresourceattribute**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




