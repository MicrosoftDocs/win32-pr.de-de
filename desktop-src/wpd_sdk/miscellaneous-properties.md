---
description: Tragbare Windows-Geräte unterstützen die folgenden verschiedenen Eigenschaften.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Sonstige Eigenschaften (portabledevice. h)
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
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354091"
---
# <a name="miscellaneous-properties"></a>Sonstige Eigenschaften

Tragbare Windows-Geräte unterstützen die folgenden verschiedenen Eigenschaften.



| Eigenschaft                                       | VarType         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD- \_ API- \_ Option \_ use \_ Clear \_ Data \_ Stream** | **VT \_ bool**    | Ein boolescher Wert, der angibt, ob der Datenstrom, der für die Datenübertragung erstellt wurde, eindeutig ist, d. h., DRM ist nicht beteiligt. Clients können diese Option festlegen, indem Sie Sie den Objekteigenschaften hinzufügen, die an [**iportabledevicecontent:: deateobjectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)übergeben werden.<br/>                                                                                                                                                   |
| **WPD- \_ Dienst \_ Version**                      | **VT \_ LPWSTR**  | Eine Zeichenfolge, die die Implementierungs Version eines bestimmten Geräte Dienstanbieter angibt.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Inhaltstypen für WPD- \_ Ordner sind \_ \_ \_ zulässig.**       | **VT \_ unbekannt** | Ein-Wert, der die Objekttypen angibt, die direkt untergeordnete Elemente dieses Ordners sein können. Untergeordnete Ordner können über unterschiedliche Funktionen verfügen. Diese Eigenschaft ist eine [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) \_ , die VT CLSID-Werte enthält, die zulässige Objekttypen angeben.<br/> Eine Liste der Objekttypen, die von tragbaren Windows-Geräten definiert werden, finden Sie unter [Anforderungen für Objekte](requirements-for-objects.md).<br/>                                         |
| **WPD- \_ Funktions \_ Objekt \_ Kategorie**          | **VT \_ CLSID**   | Ein-Wert, der die Funktions Kategorie des-Objekts angibt.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **WPD- \_ RENDERING- \_ Informations \_ profile**      | **VT \_ unbekannt** | Eine [**iportabledevicevaluescollection**](iportabledevicevaluescollection.md) , die mehrere [**iportabledevicevalues**](iportabledevicevalues.md) -Schnittstellen enthält, von denen jede die Eigenschafts Einstellungen für ein Profil enthält, das vom-Objekt unterstützt wird.                                                                                                                                                                                                                                            |
| **\_ \_ \_ \_ Anzeige \_ Name des WPD-Objekt Hinweis Speicher Orts** | **VT \_ LPWSTR**  | Wenn ein Objekt ein Hinweis Speicherort ist, gibt diese Eigenschaft den Hinweis spezifischen Namen an, der dem Benutzer anstelle des Objekt namens angezeigt werden soll. Treiber können Positions Hinweise für verschiedene Objekttypen angeben. Dies sind bevorzugte Speicherorte für Ordner, die einen bestimmten Objekttyp enthalten. Eine Entsprechung wäre der Ordner Meine Bilder für Bilddateien in Windows. Wenn diese Eigenschaft nicht vorhanden ist, wird in der Regel der [ \_ \_ Name des WPD-Objekts](object-properties.md) verwendet.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




