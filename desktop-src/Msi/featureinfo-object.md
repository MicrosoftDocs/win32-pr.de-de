---
description: Das FeatureInfo-Objekt enthält Informationen zum Zielfeature und wird mithilfe der FeatureInfo-Methode aus dem Session-Objekt erstellt.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: FeatureInfo-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 136bc160ea81367f8f55ad81cfc06f5e2e272cafae9d7b8f444a65d34e85d52b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328370"
---
# <a name="featureinfo-object"></a>FeatureInfo-Objekt

Das **FeatureInfo-Objekt** enthält Informationen zum Zielfeature und wird mithilfe der FeatureInfo-Methode aus dem [**Session-Objekt**](session-featureinfo.md) erstellt. [](session-object.md)

## <a name="members"></a>Member

Das **FeatureInfo-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **FeatureInfo-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                  | Zugriffstyp           | BESCHREIBUNG                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Attribute**](featureinfo-attributes.md)<br/>   | Lesen/Schreiben<br/> | Gibt den Wert für das Feature in der Spalte Attribute der Tabelle Feature zurück.<br/> |
| [**Beschreibung**](featureinfo-description.md)<br/> |                       | Gibt die Beschreibung des Features zurück.<br/>                                          |
| [**Titel**](featureinfo-title.md)<br/>             | Schreibgeschützt<br/>  | Gibt den Titel des Features zurück.<br/>                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IFeatureInfo ist als 000C109F-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Windows Skriptbeispiele für Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




