---
description: Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.
ms.assetid: aba78d50-f884-416a-b022-bb03416aad11
title: faultInfo-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3788af9aeb31d1ed84522bc6b177143ec0607b2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995857"
---
# <a name="faultinfo-element"></a>faultInfo-Element

Gibt an, ob Parameter, die zum Übergeben von Fehlerinformationen verwendet werden, in generierten Funktionen enthalten sind.

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



 

 




