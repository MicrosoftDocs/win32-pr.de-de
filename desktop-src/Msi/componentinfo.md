---
description: Das ComponentInfo-Objekt stellt zusätzliche Details zu einer Komponente dar, die über einen Aufruf von MsiGetComponentPathEx erhalten werden können.
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
ms.openlocfilehash: a59aa1d9f7bdc5babc29461ca90c01b6fe604482cb78ba6549e782b1e34d54b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252000"
---
# <a name="componentinfo-object"></a>ComponentInfo-Objekt

Das ComponentInfo-Objekt stellt zusätzliche Details zu einer Komponente dar, die über einen Aufruf von MsiGetComponentPathEx erhalten werden können.

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt. Dieses Objekt ist ab Windows Installer 5.0 verfügbar.

## <a name="members"></a>Member

Das **ComponentInfo-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **ComponentInfo-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                        | BESCHREIBUNG                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](componentinfo-componentcode.md)<br/> | Der Komponentencode der in Frage gestellten Komponente.<br/> |
| [**Pfad**](componentinfo-componentcode.md)<br/>          | Der Pfad der Komponente.<br/>                       |
| [**State**](componentinfo-state.md)<br/>                 | Der Zustand der Komponente.<br/>                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 oder höher.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponentInfo ist als 000C1099-0000-0000-C000-00000000046 definiert.<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verwenden der Automation-Schnittstelle](using-the-automation-interface.md)
</dt> <dt>

[Windows Skriptbeispiele für Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




