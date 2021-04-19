---
description: Das ComponentInfo-Objekt stellt zusätzliche Details zu einer Komponente dar, die über einen-Befehl von msigetcomponentpathex abgerufen werden kann.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: ComponentInfo-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368529"
---
# <a name="componentinfo-object"></a>ComponentInfo-Objekt

Das ComponentInfo-Objekt stellt zusätzliche Details zu einer Komponente dar, die über einen-Befehl von msigetcomponentpathex abgerufen werden kann.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Dieses Objekt ist ab Windows Installer 5,0 verfügbar.

## <a name="members"></a>Member

Das **ComponentInfo** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **ComponentInfo** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                        | BESCHREIBUNG                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**Componentcode**](componentinfo-componentcode.md)<br/> | Der Komponenten Code der betreffenden Komponente.<br/> |
| [**ADS**](componentinfo-componentcode.md)<br/>          | Der Pfad der Komponente.<br/>                       |
| [**State**](componentinfo-state.md)<br/>                 | Der Status der Komponente.<br/>                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 oder höher.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ icomponentinfo ist definiert als 000c1099-0000-0000-C000-000000000046<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden der Automatisierungsschnittstelle](using-the-automation-interface.md)
</dt> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




