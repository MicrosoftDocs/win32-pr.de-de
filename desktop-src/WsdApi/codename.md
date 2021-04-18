---
description: Definiert den Namen, der zum Identifizieren des Namespace in generiertem Code verwendet werden soll.
ms.assetid: 4e476be2-fa73-4b3e-b0cc-799c8d16b5de
title: Codename-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44c10b937f503c2d3994543db8852b5d7ee923b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350839"
---
# <a name="codename-element"></a>Codename-Element

Definiert den Namen, der zum Identifizieren des Namespace in generiertem Code verwendet werden soll.

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
| [**porttypeer-Deklarationen**](porttypedeclarations.md)<br/> | Generiert C-Konstante Deklarationen für Porttypen.<br/> <br/> |
| [**porttypeer Definitionen**](porttypedefinitions.md)<br/>   | Generiert C-Konstanten für Porttypen.<br/> <br/>             |



## <a name="remarks"></a>Bemerkungen

Dieses Element überschreibt den Standard Code Namen, der für generierten Code verwendet wird. Standardmäßig erstellt der generierte Code einen Codenamen aus dem URI oder dem qualifizierten Namen.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




