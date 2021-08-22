---
description: Windows Portable Devices unterstützt die folgenden verschiedenen Eigenschaften.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Verschiedene Eigenschaften (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bdc093d877a180f6c7072ff9365e96edfe7d9e2c006fdcb745c58e92df3b179f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704430"
---
# <a name="miscellaneous-properties"></a>Sonstige Eigenschaften

Windows Portable Devices unterstützt die folgenden verschiedenen Eigenschaften.



| Eigenschaft                                       | VarType         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_WPD-API-OPTION \_ ZUM VERWENDEN VON CLEAR DATA \_ \_ \_ \_ STREAM** | **VT \_ BOOL**    | A Boolean value that specifies whether the data stream created for data transfer will be clear, that is, DRM is not involved.Clients can set this option by adding it to the object properties passed to [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).<br/>                                                                                                                                                   |
| **\_WPD-DIENSTVERSION \_**                      | **VT \_ LPWSTR**  | Eine Zeichenfolge, die die Implementierungsversion eines bestimmten Gerätediensts angibt.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **\_ \_ WPD-ORDNERINHALTSTYPEN \_ \_ ZULÄSSIG**       | **VT \_ UNKNOWN** | Ein -Wert, der die Objekttypen angibt, die direkte children-Objekte dieses Ordners sein können. Untergeordnete Ordner können unterschiedliche Funktionen haben. Diese Eigenschaft ist eine [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) mit VT \_ CLSID-Werten, die zulässige Objekttypen angeben.<br/> Eine Liste der objekttypen, die von portablen Windows definiert werden, finden Sie [unter Anforderungen für Objekte.](requirements-for-objects.md)<br/>                                         |
| **WPD \_ FUNCTIONAL \_ OBJECT \_ CATEGORY**          | **VT \_ CLSID**   | Ein -Wert, der die Funktionskategorie des Objekts angibt.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **\_ \_ WPD-RENDERINGINFORMATIONSPROFILE \_**      | **VT \_ UNKNOWN** | Eine [**IPortableDeviceValuesCollection,**](iportabledevicevaluescollection.md) die mehrere [**IPortableDeviceValues-Schnittstellen**](iportabledevicevalues.md) enthält, von denen jede die Eigenschafteneinstellungen für ein Profil enthält, das das Objekt unterstützt.                                                                                                                                                                                                                                            |
| **WPD \_ OBJECT HINT LOCATION DISPLAY NAME (ANZEIGENAME DES WPD-OBJEKTHINWEISES) \_ \_ \_ \_** | **VT \_ LPWSTR**  | Wenn ein Objekt ein Hinweisspeicherort ist, gibt diese Eigenschaft den hinweisspezifischen Namen an, der dem Benutzer anstelle des Objektnamens angezeigt werden soll. Treiber können Speicherorthinweise für verschiedene Objekttypen angeben. Dies sind bevorzugte Speicherorte für Ordner, die einen bestimmten Objekttyp enthalten. Eine Entsprechung wäre der Ordner Meine Bilder für Bilddateien in Windows. Wenn diese Eigenschaft nicht vorhanden ist, wird in der Regel stattdessen [der WPD \_ OBJECT \_ NAME](object-properties.md) verwendet.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




