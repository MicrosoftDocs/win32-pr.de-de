---
description: Gibt an, ob asynchrone Vorgänge in den generierten Proxy Funktionen enthalten sind.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: Async-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea04eaa66fbdadfc784650c1a451cebf171f6372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050379"
---
# <a name="async-element"></a>Async-Element

Gibt an, ob asynchrone Vorgänge in den generierten Proxy Funktionen enthalten sind.

## <a name="usage"></a>Verbrauch

``` syntax
<async/>
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



## <a name="remarks"></a>Bemerkungen

Mögliche Werte sind 1 (asynchrone Vorgänge eingeschlossen) und 0 (standardmäßige asynchrone Vorgänge ausgeschlossen).

Ein Proxy kann sowohl asynchrone als auch synchrone Versionen der gleichen Vorgänge aufweisen.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




