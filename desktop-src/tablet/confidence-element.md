---
description: Enthält die von der Journal-Ink-Analyse für inkWord zurückgegebene Konfidenzbewertung.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Confidence-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e4169767f3bf40d49e71e84214d50d3c0c0b4ecf5d3f7a9034ee6c8ea279d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936980"
---
# <a name="confidence-element"></a>Confidence-Element

Enthält die Von der Journal-Ink-Analyse für inkWord zurückgegebene [**Konfidenzbewertung.**](inkword-element.md)

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**InkWord**](inkword-element.md)

## <a name="values"></a>Werte

Gültige Werte für dieses Feld sind "0", "1" und "2". 0 steht für Starke Konfidenz, 1 für Zwischenvertrauen und 2 für Schlechte Konfidenz.

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute

Keine

## <a name="element-information"></a>Elementinformationen



|                  | Wert                                      |
|------------------|--------------------------------------------|
| **Elementtyp** | xs:string                                  |
| **Namespace**    | urn:schemas-microsoft-com:tabletpc:richink |
| **Schemaname**  | Journalreader                             |



 

 

 



