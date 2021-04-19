---
description: Gibt an, ob wsdcodegen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: AUTOSTATIC-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32591c43c850af05014ff92fc4023e228b371fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348914"
---
# <a name="autostatic-element"></a>AUTOSTATIC-Element

Gibt an, ob wsdcodegen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen. Dieses Verhalten ist standardmäßig aktiviert.

## <a name="usage"></a>Verbrauch

``` syntax
<autoStatic/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdcodegen**](wsdcodegen.md)<br/> | Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Das **AUTOSTATIC** -Element ist nicht erforderlich und kann in der XML-Konfigurationsdatei weggelassen werden. Das-Element kann verwendet werden, um die Kennzeichnung generierter Felder als statisch zu deaktivieren oder um explizit das kennzeichnen bestimmter generierter Felder als statisch zu erzwingen.

Mögliche Werte sind 1 (aktiviert, Standard) und 0 (deaktiviert). Das Aktivieren von **AUTOSTATIC** kann Kompilierungs Probleme verursachen, abhängig davon, wie der Code Generator an Ausgabedaten weitergeleitet wird.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




