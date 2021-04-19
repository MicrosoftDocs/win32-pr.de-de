---
description: Das Component-Objekt stellt eine eindeutige Instanz einer Komponente dar, die für die Enumeration verfügbar ist.
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: Component-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351316"
---
# <a name="component-object"></a>Component-Objekt

Das Component-Objekt stellt eine eindeutige Instanz einer Komponente dar, die für die Enumeration verfügbar ist.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Dieses Objekt ist ab Windows Installer 5,0 verfügbar.

## <a name="members"></a>Member

Das **Komponenten** Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Komponenten** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                    | BESCHREIBUNG                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**Componentcode**](component-componentcode.md)<br/> | Der Komponenten Code der betreffenden Komponente.<br/>                               |
| [**Kontext**](component-context.md)<br/>             | Der Kontext, der für die Anwendung auf die betreffende Komponente bestimmt wurde.<br/> |
| [**UserSID**](component-usersid.md)<br/>             | Die Benutzer-SID für die aufgelistete Komponente.<br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 oder höher.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponent ist definiert als 000c1097-0000-0000-C000-000000000046<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden der Automatisierungsschnittstelle](using-the-automation-interface.md)
</dt> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




