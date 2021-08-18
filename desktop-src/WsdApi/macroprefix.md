---
description: Definiert das Präfix, das im generierten Code für Namen von Makros im Namespace verwendet werden soll.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: macroPrefix-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 970232b86aa226f16fa06cf2d3c9de40c156702c802c6f6254e45157e1df58ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130712"
---
# <a name="macroprefix-element"></a>macroPrefix-Element

Definiert das Präfix, das im generierten Code für Namen von Makros im Namespace verwendet werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<macroPrefix/>
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

Dieses Element überschreibt das Standard-URI-Präfix, das für generierte Makros verwendet wird. Wenn das Makropräfix beispielsweise \_ "AV" und der Name "Tuner" lautet, lautet das für den qualifizierten Namen generierte Makro "AV \_ Tuner".

Standardmäßig erstellt der generierte Code ein bevorzugtes Makropräfix aus dem URI.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




