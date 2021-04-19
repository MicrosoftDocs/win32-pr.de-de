---
description: Das FeatureInfo-Objekt enthält Informationen zur Zielfunktion und wird mithilfe der FeatureInfo-Methode aus dem Sitzungs Objekt erstellt.
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
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367425"
---
# <a name="featureinfo-object"></a>FeatureInfo-Objekt

Das **FeatureInfo** -Objekt enthält Informationen zur Zielfunktion und wird mithilfe der [**FeatureInfo**](session-featureinfo.md) -Methode aus dem [**Sitzungs**](session-object.md) Objekt erstellt.

## <a name="members"></a>Member

Das **FeatureInfo** -Objekt verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **FeatureInfo** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                  | Zugriffstyp           | BESCHREIBUNG                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Attribute**](featureinfo-attributes.md)<br/>   | Lesen/Schreiben<br/> | Gibt den Wert für die Funktion in der Spalte Attribute der Funktions Tabelle zurück.<br/> |
| [**Beschreibung**](featureinfo-description.md)<br/> |                       | Gibt die Beschreibung der Funktion zurück.<br/>                                          |
| [**Titel**](featureinfo-title.md)<br/>             | Schreibgeschützt<br/>  | Gibt den Titel der Funktion zurück.<br/>                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ifeatureinfo ist definiert als 000c109f-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skript Beispiele für Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




