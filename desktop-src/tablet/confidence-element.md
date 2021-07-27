---
description: Enthält die Von der Journal-Ink-Analyse für inkWord zurückgegebene Konfidenzbewertung.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Confidence-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fdaaed8d9c57822ad94ec49183a399ed317917
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436498"
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



 

 

 



