---
description: Generiert IDL-Deklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: subscriptionIdlFunctionDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3998103d04250206ef382f822e329210b83471c69dcc51b401fcfbc241460729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130612"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a>subscriptionIdlFunctionDeclarations-Element

Generiert IDL-Deklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.

## <a name="usage"></a>Verbrauch

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a>Attribute



| attribute                 | type               | Erforderlich      | Beschreibung                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Extensible**<br/> | boolean<br/> | Nein<br/> | Die Möglichkeit, Erweiterungspunkte zu Funktionen und Schnittstellen hinzuzufügen. Dieser Wert ist immer auf TRUE festgelegt.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                           | Beschreibung                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**notificationInterface**](notificationinterface.md)<br/> | Gibt den Namen der Benachrichtigungsschnittstelle an, die mit Ereignisabonnements verwendet wird.<br/> <br/> |
| [**Vorgang**](operation.md)<br/>                         | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                       |
| [**Porttype**](porttype.md)<br/>                           | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                      |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | Beschreibung                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




