---
description: Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: faultInfo-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 921a7dedfffbe7bfb3e402775258636ed9ccd3e74c72d65a5c76cea40d7ed4b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049678"
---
# <a name="faultinfo-element"></a>faultInfo-Element

Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.

## <a name="usage"></a>Verwendung

``` syntax
<faultInfo/>
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
| [**stubDefinitions**](stubdefinitions.md)<br/>                           | Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.<br/> <br/>              |



## <a name="remarks"></a>Hinweise

Mögliche Werte sind 1 (Fehlerparameter eingeschlossen) und 0 (Fehlerparameter ausgeschlossen). Standardmäßig werden Fehlerparameter ausgeschlossen.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




