---
description: Das configurableitem-Objekt stellt eine einzelne Zeile aus der Tabelle ModuleConfiguration dar.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Configurableitem-Objekt (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365782"
---
# <a name="configurableitem-object"></a>Configurableitem-Objekt

Das **configurableitem-Objekt** stellt eine einzelne Zeile aus der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)dar. Dabei handelt es sich um ein einzelnes konfigurierbares "Attribut" aus dem Modul. Die-Schnittstelle besteht aus schreibgeschützten Eigenschaften, eine für jede Spalte in der ModuleConfiguration-Tabelle. Die Schnittstellen Definition lautet wie folgt.

## <a name="members"></a>Member

Das **configurableitem** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **configurableitem** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                         | BESCHREIBUNG                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attribute**](configurableitem-attributes.md)<br/>     | Gibt den Wert im Feld Attribute des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                            |
| [**Kontext**](configurableitem-context.md)<br/>           | Gibt den Wert im Kontext Feld des Datensatzes dieses Objekts in der ModuleConfiguration-Tabelle zurück.<br/>                               |
| [**DefaultValue**](configurableitem-defaultvalue.md)<br/> | Gibt den Wert im DefaultValue-Feld des Datensatzes dieses Objekts in der ModuleConfiguration-Tabelle zurück.<br/>                          |
| [**Beschreibung**](configurableitem-description.md)<br/>   | Gibt den Wert im Beschreibungsfeld des Datensatzes dieses Objekts in der ModuleConfiguration-Tabelle zurück.<br/>                           |
| [**DisplayName**](configurableitem-displayname.md)<br/>   | Gibt den Wert im Feld Display Name des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                           |
| [**Ges**](configurableitem-format.md)<br/>             | Gibt den Wert im Feld Format des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                                |
| [**HelpKeyword**](configurableitem-helpkeyword.md)<br/>   | Gibt den Wert im Feld HelpKeyword des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                           |
| [**Helplocation**](configurableitem-helplocation.md)<br/> | Gibt den Wert im Feld helplocation des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                          |
| [**Name**](configurableitem-name.md)<br/>                 | Gibt den Wert im Feld Name des Datensatzes dieses Objekts in der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)zurück.<br/> |
| [**type**](configurableitem-type.md)<br/>                 | Gibt den Wert im type-Feld des Datensatzes dieses Objekts in der ModuleConfiguration-Tabelle zurück.<br/>                                  |



 

## <a name="c"></a>C++

Schnittstelle **imsmconfigurableitem: IDispatch**

## <a name="interface-id"></a>Schnittstellen-ID



| Konstante                      | Wert                                  |
|-------------------------------|----------------------------------------|
| **IID \_ imsmconfigurableitem** | {4d6e6284-d21d-401E-84b6-909e00b50f 71} |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




