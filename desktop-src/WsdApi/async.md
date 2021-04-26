---
description: Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.
ms.assetid: 7b57d5c6-589b-4e03-bfcf-1faa671ebd77
title: async-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6cbc68d0a5dea30f4b4d179a54539ac3f9516a4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994957"
---
# <a name="async-element"></a>async-Element

Gibt an, ob asynchrone Vorgänge in den generierten Proxyfunktionen enthalten sind.

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



 

 




