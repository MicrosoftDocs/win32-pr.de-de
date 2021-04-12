---
description: Generiert Implementierungs Deklarationen für Abonnement-/abonnementproxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.
ms.assetid: 0e5b2232-c9bf-4741-921d-bb3bce4ee293
title: abonnemenfunctiondeklarationen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8957dcec6133d98830659fa76e2b7939079d3c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218811"
---
# <a name="subscriptionfunctiondeclarations-element"></a>abonnemenfunctiondeklarationen-Element

Generiert Implementierungs Deklarationen für Abonnement-/abonnementproxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.

## <a name="usage"></a>Verbrauch

``` syntax
<subscriptionFunctionDeclarations
  extensible = "boolean">
  child elements
</subscriptionFunctionDeclarations>
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



 

 




