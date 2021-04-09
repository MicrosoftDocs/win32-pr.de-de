---
description: Generiert IDL-Deklarationen für Abonnement-/abonnementproxyfunktionen für Port-Benachrichtigungs Vorgänge.
ms.assetid: 240ef2b3-ed72-45bb-b653-441c4e5540b5
title: abonnemenidlfunctiondeklarationselement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1eba60e327778efb1589436a09e62d043d2960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867603"
---
# <a name="subscriptionidlfunctiondeclarations-element"></a>abonnemenidlfunctiondeklarationselement

Generiert IDL-Deklarationen für Abonnement-/abonnementproxyfunktionen für Port-Benachrichtigungs Vorgänge.

## <a name="usage"></a>Verbrauch

``` syntax
<subscriptionIdlFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionIdlFunctionDeclarations>
```

## <a name="attributes"></a>Attribute



| Attribut                 | type               | Erforderlich      | BESCHREIBUNG                                                                                                                   |
|---------------------------|--------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Extensible**<br/> | boolean<br/> | Nein<br/> | Die Möglichkeit, Erweiterbarkeits Punkte Funktionen und Schnittstellen hinzuzufügen. Dieser Wert ist immer auf "true" festgelegt.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                           | BESCHREIBUNG                                                                                            |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**notificationinterface**](notificationinterface.md)<br/> | Gibt den Namen der Benachrichtigungs Schnittstelle an, die mit Ereignis Abonnements verwendet wird.<br/> <br/> |
| [**Betriebs**](operation.md)<br/>                         | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                       |
| [**PortType**](porttype.md)<br/>                           | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                      |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  notificationInterface?
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




