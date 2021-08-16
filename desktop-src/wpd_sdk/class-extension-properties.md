---
description: Windows Portable Geräte unterstützen die folgenden Klassenerweiterungseigenschaften.
ms.assetid: 9b8983ba-5824-495d-868f-fd22b98e1954
title: Klassenerweiterungseigenschaften (PortableDevice.h)
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
ms.openlocfilehash: 4c7215a383aec582f576cb64a6781068034bb7fa8df03b5a404368482f1c1619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843404"
---
# <a name="class-extension-properties"></a>Klassenerweiterungseigenschaften

Windows Portable Geräte unterstützen die folgenden Klassenerweiterungseigenschaften.



| Eigenschaft                                                                      | VarType         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ WPD-KLASSENERWEITERUNGSOPTIONEN \_ UNTERSTÜTZTE \_ \_ INHALTSTYPEN**                 | **VT \_ UNKNOWN** | Ein -Wert, der die (obere) Liste der vom Treiber unterstützten Inhaltstypen angibt (ähnlich dem Aufrufen von \_ WPD-BEFEHLSFUNKTIONEN \_ GET SUPPORTED CONTENT TYPES on \_ \_ \_ \_ **WPD FUNCTIONAL CATEGORY \_ \_ \_ ALL**).                                                                                                                                                                                                                                                                                                                                             |
| **\_WPD-KLASSENERWEITERUNGSOPTIONEN \_ \_ REGISTRIEREN KEINE \_ \_ \_ \_ WPD-GERÄTESCHNITTSTELLE \_**    | **VT \_ BOOL**    | Ein -Wert, der angibt, ob der Aufrufer möchte, dass die WPD-Klassenerweiterungsbibliothek die WPD-Geräteklassenschnittstelle registriert. Wenn dieser Wert true ist, übernimmt der Aufrufer die Verantwortung für die Registrierung.<br/> Wenn dieser Wert FALSE ist, gibt er an, dass der Aufrufer erwartet, dass die Klassenerweiterungsbibliothek die Registrierung ausführt.<br/>Die meisten Treiber sollten es der Klassenerweiterungsbibliothek ermöglichen, die Registrierung durchzuführen, es sei denn, die Registrierung der WPD-Geräteklassenschnittstelle durch die Klassenerweiterungsbibliothek kann negative Auswirkungen haben. |
| **\_WPD-KLASSENERWEITERUNGSOPTIONEN \_ \_ REGISTER \_ \_ WPD PRIVATE DEVICE \_ \_ \_ INTERFACE** | **VT \_ BOOL**    | Gibt an, dass der Aufrufer möchte, dass die WPD-Klassenerweiterungsbibliothek die private WPD-Geräteklassenschnittstelle registriert. Dies wird für die meisten Treiber nicht empfohlen. Sie sollte nur in Fällen verwendet werden, in denen die Registrierung der WPD-Geräteklassenschnittstelle durch die Klassenerweiterungsbibliothek negative Auswirkungen hat. Diese Option wird in der Regel in Verbindung mit **WPD \_ CLASS EXTENSION OPTIONS \_ \_ \_ DONT REGISTER \_ \_ WPD DEVICE \_ \_ INTERFACE** set to **TRUE** verwendet.                                                                                          |
| **\_WPD-KLASSENERWEITERUNGSOPTIONEN \_ \_ \_ \_ GERÄTEIDENTIFIKATIONSWERTE \_**            | **VT \_ UNKNOWN** | Dies ist ein [IPortableDeviceValues-Objekt,](iportabledevicevalues.md) das die Geräteidentifikationswerte enthält (**\_ WPD-GERÄTEHERSTELLER, \_** **\_ WPD-GERÄTEMODELL, \_** **\_ WPD-GERÄTEFIRMWAREVERSION \_ \_** und **WPD \_ DEVICE FUNCTIONAL UNIQUE \_ \_ \_ ID**). Schließen Sie dies bei der Initialisierung mit anderen Klassenerweiterungsoptionen ein.                                                                                                                                                                                                                               |
| **\_WPD-KLASSENERWEITERUNGSOPTIONEN \_ \_ \_ \_ TRANSPORTBANDBREITE**                      | **VT \_ UI4**     | Gibt die theoretische maximale Bandbreite des Transports in Kilobits pro Sekunde an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **\_WPD-KLASSENERWEITERUNGSOPTIONEN \_ \_ \_ \_ GERÄTEIDENTIFIKATIONSWERTE \_**            | **VT \_ UNKNOWN** | Dies ist ein [IPortableDeviceValues-Objekt,](iportabledevicevalues.md) das die Geräteidentifikationswerte enthält (**\_ WPD-GERÄTEHERSTELLER, \_** **\_ WPD-GERÄTEMODELL, \_** **\_ WPD-GERÄTEFIRMWAREVERSION \_ \_** und **WPD \_ DEVICE FUNCTIONAL UNIQUE \_ \_ \_ ID**). Schließen Sie dies bei der Initialisierung mit anderen Klassenerweiterungsoptionen ein.                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




