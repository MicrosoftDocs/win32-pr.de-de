---
description: Tragbare Windows-Geräte unterstützen die folgenden Klassen Erweiterungs Eigenschaften.
ms.assetid: 9b8983ba-5824-495d-868f-fd22b98e1954
title: Klassen Erweiterungs Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Class
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c7e961b80ae990653e6c354640b35c28f8bcf8b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371027"
---
# <a name="class-extension-properties"></a>Klassen Erweiterungs Eigenschaften

Tragbare Windows-Geräte unterstützen die folgenden Klassen Erweiterungs Eigenschaften.



| Eigenschaft                                                                      | VarType         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ \_ unterstützte \_ Inhalts \_ Typen für WPD-Klassen Erweiterungsoptionen**                 | **VT \_ unbekannt** | Ein-Wert, der die (Superset)-Liste der vom Treiber unterstützten Inhaltstypen angibt (ähnlich wie das Aufrufen von WPD- \_ Befehls \_ Funktionen, \_ werden \_ unterstützte \_ Inhalts \_ Typen in der **WPD- \_ Funktions \_ Kategorie \_ alle** angezeigt).                                                                                                                                                                                                                                                                                                                                             |
| **WPD- \_ Klassen \_ Erweiterungsoptionen keine \_ \_ \_ \_ WPD- \_ Geräte \_ Schnittstelle registrieren**    | **VT \_ bool**    | Ein Wert, der angibt, ob der Aufrufer die WPD-Klassen-Erweiterungs Bibliothek zum Registrieren der WPD-Geräteklassen Schnittstelle benötigt. Wenn dieser Wert true ist, übernimmt der Aufrufer die Verantwortung für die Registrierung.<br/> Wenn dieser Wert false ist, gibt dies an, dass der Aufrufer erwartet, dass die Klassen Erweiterungs Bibliothek die Registrierung durchführt.<br/>Die meisten Treiber sollten der Klassen Erweiterungs Bibliothek gestatten, die Registrierung auszuführen, außer wenn das Registrieren der WPD-Geräteklassen Schnittstelle durch die Klassen Erweiterungs Bibliothek zu negativen Auswirkungen führen kann. |
| **WPD- \_ Klassen \_ Erweiterungs \_ Optionen Registrieren der \_ \_ privaten WPD- \_ \_ Geräte \_ Schnittstelle** | **VT \_ bool**    | Gibt an, dass der Aufrufer möchte, dass die WPD-Klassen Erweiterungs Bibliothek die private WPD-Geräteklassen Schnittstelle registriert. Dies ist für die meisten Treiber nicht empfehlenswert. Sie sollte nur in Fällen verwendet werden, in denen die Registrierung der WPD-Geräteklassen Schnittstelle durch die Klassen Erweiterungs Bibliothek zu negativen Auswirkungen führt. Diese Option wird in der Regel in Verbindung mit **WPD- \_ Klassen \_ Erweiterungs \_ Optionen nicht \_ \_ registrieren \_ WPD- \_ Geräte \_ Schnittstelle** auf **true** festgelegt.                                                                                          |
| **WPD- \_ Klassen \_ Erweiterungs \_ Optionen \_ Geräte \_ Identifikations \_ Werte**            | **VT \_ unbekannt** | Dies ist ein [iportabledevicevalues](iportabledevicevalues.md) -Element, das die Geräte Identifikations Werte (**WPD- \_ Geräte \_ Hersteller**, **WPD-Geräte \_ \_ Modell**, **WPD- \_ Geräte \_ \_** Firmwareversion und **eindeutige WPD- \_ Geräte Funktions- \_ \_ \_ ID**) enthält. Diese bei der Initialisierung mit anderen Klassen Erweiterungsoptionen einschließen                                                                                                                                                                                                                               |
| **WPD- \_ Klassen \_ Erweiterungs \_ Optionen \_ Transport \_ Bandbreite**                      | **VT \_ UI4**     | Gibt die theoretische maximale Bandbreite des Transports in Kbit pro Sekunde an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **WPD- \_ Klassen \_ Erweiterungs \_ Optionen \_ Geräte \_ Identifikations \_ Werte**            | **VT \_ unbekannt** | Dies ist ein [iportabledevicevalues](iportabledevicevalues.md) -Element, das die Geräte Identifikations Werte (**WPD- \_ Geräte \_ Hersteller**, **WPD-Geräte \_ \_ Modell**, **WPD- \_ Geräte \_ \_** Firmwareversion und **eindeutige WPD- \_ Geräte Funktions- \_ \_ \_ ID**) enthält. Schließen Sie dies mit anderen Klassen Erweiterungsoptionen bei der Initialisierung ein.                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




