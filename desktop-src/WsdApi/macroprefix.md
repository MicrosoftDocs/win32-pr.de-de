---
description: Definiert das Präfix, das im generierten Code für Die Namen von Makros im Namespace verwendet werden soll.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: macroPrefix-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9590092d78ea4700715a868bb7e50f15833011
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998747"
---
# <a name="macroprefix-element"></a>macroPrefix-Element

Definiert das Präfix, das im generierten Code für Die Namen von Makros im Namespace verwendet werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<macroPrefix/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                        |
|-------------------------------------------|--------------------------------------------------------------------|
| [**Namespace**](namespace.md)<br/> | Ein Namespace, der für die Codegenerierung verwendet werden soll.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Element überschreibt das Standard-URI-Präfix, das für generierte Makros verwendet wird. Wenn das Makropräfix beispielsweise "AV" und der Name "Tuner" ist, ist das für den qualifizierten Namen generierte Makro \_ "AV \_ Tuner".

Standardmäßig erstellt der generierte Code ein bevorzugtes Makropräfix aus dem URI.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




