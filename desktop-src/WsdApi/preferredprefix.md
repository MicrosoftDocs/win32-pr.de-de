---
description: Definiert das Präfix, dem der Namespace zugeordnet werden soll, um den XML-Code lesbarer zu machen.
ms.assetid: 955f4785-5657-4a89-9728-bce99a0a4234
title: preferredprefix-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71f124756f29aaf29ba30d254f9b03ab4495f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356644"
---
# <a name="preferredprefix-element"></a>preferredprefix-Element

Definiert das Präfix, dem der Namespace zugeordnet werden soll, um den XML-Code lesbarer zu machen.

## <a name="usage"></a>Verbrauch

``` syntax
<preferredPrefix/>
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

Dieses Element überschreibt das Standard-URI-Präfix, das für generierten Code verwendet wird. Ein medienbezogener Namespace könnte z. b. das bevorzugte Präfix "AV" (für Audiodaten und Visualisierungen) enthalten.

Standardmäßig erstellt der generierte Code ein bevorzugtes Präfix aus dem URI.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




