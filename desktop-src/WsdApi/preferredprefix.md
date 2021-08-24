---
description: Definiert das Präfix, dem der Namespace zugeordnet werden soll, damit der XML-Code besser lesbar ist.
ms.assetid: 955f4785-5657-4a89-9728-bce99a0a4234
title: preferredPrefix-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934e82caf0558ff3ffc1079d3773453673bcbe916a518f6196670f37744fdf8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756870"
---
# <a name="preferredprefix-element"></a>preferredPrefix-Element

Definiert das Präfix, dem der Namespace zugeordnet werden soll, damit der XML-Code besser lesbar ist.

## <a name="usage"></a>Verbrauch

``` syntax
<preferredPrefix/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                   | Beschreibung                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [**Namespace**](namespace.md)<br/> | Ein Namespace, der für die Codegenerierung verwendet werden soll.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Element überschreibt das Standard-URI-Präfix, das für generierten Code verwendet wird. Beispielsweise kann ein medienbezogener Namespace das bevorzugte Präfix "av" (für Audio/Visual) aufweisen.

Standardmäßig erstellt der generierte Code ein bevorzugtes Präfix aus dem URI.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




