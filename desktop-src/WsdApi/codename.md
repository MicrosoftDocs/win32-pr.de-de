---
description: Definiert den Namen, der verwendet werden soll, um den Namespace im generierten Code zu identifizieren.
ms.assetid: 4e476be2-fa73-4b3e-b0cc-799c8d16b5de
title: codeName-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e778e6d55e9902ec03597d7776afce9850a93be18f578416246908310fa666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991770"
---
# <a name="codename-element"></a>codeName-Element

Definiert den Namen, der verwendet werden soll, um den Namespace im generierten Code zu identifizieren.

## <a name="usage"></a>Verbrauch

``` syntax
<codeName/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                         | BESCHREIBUNG                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**Namespace**](namespace.md)<br/>                       | Ein Namespace, der für die Codegenerierung verwendet werden soll.<br/> <br/>       |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/> | Generiert C-Konstantendeklarationen für Porttypen.<br/> <br/> |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>   | Generiert C-Konstanten für Porttypen.<br/> <br/>             |



## <a name="remarks"></a>Hinweise

Dieses Element überschreibt den Standardcodenamen, der für generierten Code verwendet wird. Standardmäßig erstellt der generierte Code einen Codenamen aus dem URI oder qualifizierten Namen.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




