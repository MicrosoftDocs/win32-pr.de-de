---
description: Windows Portable Geräte unterstützen die folgenden Ressourcenattributeigenschaften.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Ressourcenattributeigenschaften (PortableDevice.h)
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
ms.openlocfilehash: 956cd349089afb00a1350bf32e8f06acd5747599f6d5a731e4bf5d8dd1c96295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928070"
---
# <a name="resource-attribute-properties"></a>Ressourcenattributeigenschaften

Windows Portable Geräte unterstützen die folgenden Ressourcenattributeigenschaften.



| Eigenschaft                                    | VarType         | Beschreibung                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RESSOURCENSCHLÜSSEL DES \_ \_ WPD-RESSOURCENATTRIBUTS \_ \_** | **VT \_ UNKNOWN** | Dies ist eine [**IPortableDeviceKeyCollection,**](iportabledevicekeycollection.md) die einen einzelnen Wert enthält, der der Schlüssel ist, der die Ressource identifiziert.                     |
| **\_ \_ WPD-RESSOURCENATTRIBUTFORMAT \_**        | **VT \_ CLSID**   | Ein GUID-Wert, der das Format der Ressource angibt. Unter [Objektformate](object-format-guids.md) finden Sie eine Liste der Formate, die von portablen Windows definiert werden. |
| **\_ \_ WPD-RESSOURCENATTRIBUT \_ \_ GESAMTGRÖßE**   | **VT \_ UI8**     | Die Gesamtgröße der Ressourcendaten in Bytes.                                                                                                                            |



 

## <a name="remarks"></a>Hinweise

Diese Attribute werden von der [**IPortableDeviceResources::GetResourceAttributes-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




