---
description: Generiert Implementierungen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: subscriptionProxyFunctionImplementations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0abc98e0e9bebd4ff2185d669402c0dae025c07bc4af84be3116dda97b6657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991570"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a>subscriptionProxyFunctionImplementations-Element

Generiert Implementierungen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.

## <a name="usage"></a>Verbrauch

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
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
| [**proxyClass**](proxyclass.md)<br/>                       | Gibt den Namen der clientseitigen Proxyklasse an.<br/> <br/>                              |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  proxyClass?, 
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



 

 




