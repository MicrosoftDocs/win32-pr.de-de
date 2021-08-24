---
description: Windows Portable Geräte unterstützen die dateneigenschaften im folgenden Abschnitt.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Eigenschaften des Abschnittsattributs (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 21c2386175fe2c3117afd722bd9a6762b605acbc51e299d33934d161974db796
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704330"
---
# <a name="section-attribute-properties"></a>Abschnittsattributeigenschaften

Windows Portable Geräte unterstützen die dateneigenschaften im folgenden Abschnitt.



| Eigenschaft                                             | VarType         | Beschreibung                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DATENLÄNGE DES WPD-ABSCHNITTS \_ \_**                       | **VT \_ UI8**     | Gibt die Länge des Objekts an, auf das verwiesen wird.                                                                                                                                                                                                                                                                                              |
| **\_DATENOFFSET DES WPD-ABSCHNITTS \_ \_**                       | **VT \_ UI8**     | Gibt den nullbasierten Offset der Daten für das Objekt an, auf das verwiesen wird.                                                                                                                                                                                                                                                                      |
| **OBJEKTRESSOURCE IM \_ WPD-ABSCHNITTSDATENVERWEIS \_ \_ \_ \_** | **VT \_ UNKNOWN** | Eine [**IPortableDeviceKeyCollection,**](iportabledevicekeycollection.md) die einen einzelnen Wert enthält, der den Schlüssel für eine bestimmte Ressource angibt. Diese Ressource ist das Objekt, auf das von WPD SECTION DATA OFFSET und WPD SECTION DATA LENGTH verwiesen \_ \_ \_ \_ \_ \_ wird.<br/> Wenn diese Eigenschaft nicht vorhanden ist, wird WPD \_ RESOURCE \_ DEFAULT angenommen.<br/> |
| **\_DATENEINHEITEN IM WPD-ABSCHNITT \_ \_**                        | **VT \_ UI4**     | Gibt die für diesen Offset verwendeten Einheiten an, z. B. Bytes, Millisekunden usw. Die möglichen Werte für diese Eigenschaft werden in der **WPD \_ SECTION DATA \_ UNITS \_ \_ VALUES-Enumeration** in der Datei PortableDevice.h definiert.<br/> Wenn keine Einheiten angegeben werden, werden Bytes angenommen.<br/>                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




