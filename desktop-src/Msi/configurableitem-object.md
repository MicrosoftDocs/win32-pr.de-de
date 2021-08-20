---
description: Das ConfigurableItem-Objekt stellt eine einzelne Zeile aus der Tabelle ModuleConfiguration dar.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: ConfigurableItem-Objekt (Mergemod.h)
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
ms.openlocfilehash: fa0ade829cff2359e074a4c2faf9942e94aa5e063f0cce841a5a0f0a84a5f3e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143729"
---
# <a name="configurableitem-object"></a>ConfigurableItem-Objekt

Das **ConfigurableItem-Objekt** stellt eine einzelne Zeile aus der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)dar. Dies ist ein einzelnes konfigurierbares "Attribut" aus dem Modul. Die Schnittstelle besteht aus schreibgeschützten Eigenschaften, eine für jede Spalte in der Tabelle ModuleConfiguration. Die Schnittstellendefinition lautet wie folgt.

## <a name="members"></a>Member

Das **ConfigurableItem-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **ConfigurableItem-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                         | Beschreibung                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Attribute**](configurableitem-attributes.md)<br/>     | Gibt den Wert im Feld Attribute des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                            |
| [**Kontext**](configurableitem-context.md)<br/>           | Gibt den Wert im Feld Kontext des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                               |
| [**Defaultvalue**](configurableitem-defaultvalue.md)<br/> | Gibt den Wert im Feld DefaultValue des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                          |
| [**Beschreibung**](configurableitem-description.md)<br/>   | Gibt den Wert im Feld Beschreibung des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                           |
| [**DisplayName**](configurableitem-displayname.md)<br/>   | Gibt den Wert im Feld DisplayName des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                           |
| [**Format**](configurableitem-format.md)<br/>             | Gibt den Wert im Feld Format des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                                |
| [**Helpkeyword**](configurableitem-helpkeyword.md)<br/>   | Gibt den Wert im Feld HelpKeyword des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                           |
| [**HelpLocation**](configurableitem-helplocation.md)<br/> | Gibt den Wert im Feld HelpLocation des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                          |
| [**Name**](configurableitem-name.md)<br/>                 | Gibt den Wert im Feld Name des Datensatzes dieses Objekts in der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)zurück.<br/> |
| [**Typ**](configurableitem-type.md)<br/>                 | Gibt den Wert im Feld Type des Datensatzes dieses Objekts in der Tabelle ModuleConfiguration zurück.<br/>                                  |



 

## <a name="c"></a>C++

schnittstelle **IMsmConfigurableItem : IDispatch**

## <a name="interface-id"></a>Schnittstellen-ID



| Konstante                      | Wert                                  |
|-------------------------------|----------------------------------------|
| **IID \_ IMsmConfigurableItem** | {4D6E6284-D21D-401E-84F6-909E00B50F71} |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




