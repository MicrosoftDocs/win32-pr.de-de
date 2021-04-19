---
description: Definiert das Präfix, das im generierten Code für Namen von Makros im-Namespace verwendet werden soll.
ms.assetid: ead82070-5546-4036-bff2-8da2714d4264
title: macroprefix-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76c88dc48505e3344db1467463a9a99639edd881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345269"
---
# <a name="macroprefix-element"></a>macroprefix-Element

Definiert das Präfix, das im generierten Code für Namen von Makros im-Namespace verwendet werden soll.

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



## <a name="remarks"></a>Bemerkungen

Dieses Element überschreibt das Standard-URI-Präfix, das für generierte Makros verwendet wird. Wenn das Makro Präfix z. b. "AV \_ " lautet und der Name "Tuner" lautet, ist das für den qualifizierten Namen generierte Makro "AV- \_ Tuner".

Standardmäßig erstellt der generierte Code ein bevorzugtes Makro Präfix aus dem URI.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




