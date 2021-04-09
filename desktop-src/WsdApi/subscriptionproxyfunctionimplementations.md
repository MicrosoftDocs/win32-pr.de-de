---
description: Generiert Implementierungen für Abonnement-/Abonnement-Proxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.
ms.assetid: aa26a3f1-df1e-4caa-9ada-6f4a6627b6b8
title: abonnemenproxyfunctionimplementierungen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb57fa21910f9b39440257bc72918519b35c6a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129100"
---
# <a name="subscriptionproxyfunctionimplementations-element"></a>abonnemenproxyfunctionimplementierungen-Element

Generiert Implementierungen für Abonnement-/Abonnement-Proxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.

## <a name="usage"></a>Verbrauch

``` syntax
<subscriptionProxyFunctionImplementations
  extensible = "boolean">
  child elements
</subscriptionProxyFunctionImplementations>
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
| [**proxyClass**](proxyclass.md)<br/>                       | Gibt den Namen der Client seitigen Proxy Klasse an.<br/> <br/>                              |



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



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




