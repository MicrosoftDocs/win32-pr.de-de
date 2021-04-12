---
description: Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: faultinfo-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f0fd65a7214f61a0b2fa6bb8f44d9a8cadbef07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216513"
---
# <a name="faultinfo-element"></a>faultinfo-Element

Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierte Funktionen eingeschlossen werden

## <a name="usage"></a>Verbrauch

``` syntax
<faultInfo/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                         | BESCHREIBUNG                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**functiondeklarationen**](functiondeclarations.md)<br/>                 | Generiert Implementierungs Deklarationen für Proxy Funktionen für Porttyp Vorgänge.<br/> <br/> |
| [**idlfunctiondeklarationen**](idlfunctiondeclarations.md)<br/>           | Generiert IDL-Deklarationen für Proxy Funktionen für Porttyp Vorgänge.<br/> <br/>            |
| [**proxyfunctionimplementierungen**](proxyfunctionimplementations.md)<br/> | Generiert Implementierungen für Proxy Funktionen für Porttyp Vorgänge.<br/> <br/>             |
| [**stubdefinitionen**](stubdefinitions.md)<br/>                           | Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.<br/> <br/>              |



## <a name="remarks"></a>Bemerkungen

Mögliche Werte sind 1 (Fehler Parameter eingeschlossen) und 0 (Fehler Parameter ausgeschlossen). Standardmäßig werden Fehler Parameter ausgeschlossen.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




