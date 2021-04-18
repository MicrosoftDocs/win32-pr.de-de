---
description: Tragbare Windows-Geräte unterstützen die folgenden Abschnitts Daten Eigenschaften.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Abschnitts Attribut Eigenschaften (portabledevice. h)
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
ms.openlocfilehash: 383e2e50aa5d2a922ad50609e316b3dc9905cc38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371741"
---
# <a name="section-attribute-properties"></a>Eigenschaften des Abschnitts Attributs

Tragbare Windows-Geräte unterstützen die folgenden Abschnitts Daten Eigenschaften.



| Eigenschaft                                             | VarType         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ Daten \_ Länge des WPD-Abschnitts**                       | **VT \_ UI8**     | Gibt die Länge des Objekts an, auf das verwiesen wird.                                                                                                                                                                                                                                                                                              |
| **\_ \_ Daten \_ Offset für WPD-Abschnitt**                       | **VT \_ UI8**     | Gibt den NULL basierten Offset der Daten für das Objekt an, auf das verwiesen wird.                                                                                                                                                                                                                                                                      |
| **\_ \_ \_ referenzierte \_ Objekt \_ Ressource für WPD-Abschnitts Daten** | **VT \_ unbekannt** | Eine [**iportabledevicekeycollection**](iportabledevicekeycollection.md) mit einem einzelnen Wert, der den Schlüssel für eine bestimmte Ressource angibt. Diese Ressource ist das Objekt, auf das im WPD-Abschnitts Daten \_ \_ \_ Offset und der WPD- \_ Abschnitts \_ Daten \_ Länge verwiesen wird.<br/> Wenn diese Eigenschaft nicht vorhanden ist, wird der Standardwert für die WPD- \_ Ressource \_ angenommen.<br/> |
| **\_ \_ Daten \_ Einheiten für WPD-Abschnitt**                        | **VT \_ UI4**     | Gibt die für diesen Offset verwendeten Einheiten an, z. b. bytes, Millisekunden usw. Die möglichen Werte für diese Eigenschaft werden im **WPD- \_ Abschnitt \_ \_ Dateneinheiten \_ Werte** Enumeration in der Datei portabledevice. h definiert.<br/> Wenn keine Einheiten angegeben werden, werden die Bytes angenommen.<br/>                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




