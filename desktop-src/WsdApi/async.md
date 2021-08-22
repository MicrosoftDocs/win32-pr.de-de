---
description: Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: async-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2597e0ed22fe9ccefa053891c0bd67ee76fae567847925de74faa1513de5faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049718"
---
# <a name="async-element"></a>async-Element

Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.

## <a name="usage"></a>Verwendung

``` syntax
<async/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                         | Beschreibung                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**functionDeclarations**](functiondeclarations.md)<br/>                 | Generiert Implementierungsdeklarationen für Proxyfunktionen für Porttypvorgänge.<br/> <br/> |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>           | Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.<br/> <br/>            |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/> | Generiert Implementierungen für Proxyfunktionen für Porttypvorgänge.<br/> <br/>             |



## <a name="remarks"></a>Hinweise

Mögliche Werte sind 1 (asynchrone Vorgänge eingeschlossen) und 0 (Standard, asynchrone Vorgänge ausgeschlossen).

Ein Proxy kann sowohl asynchrone als auch synchrone Versionen der gleichen Vorgänge haben.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




