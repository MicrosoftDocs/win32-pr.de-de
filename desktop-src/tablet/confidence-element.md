---
description: Enthält die von der Journal-Ink-Analyse für das InkWord zurückgegebene Vertrauenswürdigkeit.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Confidence-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cef4869776a6cafc4e6ef4758649b918e0b5988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128132"
---
# <a name="confidence-element"></a>Confidence-Element

Enthält die von der Journal-Ink-Analyse für das [**InkWord**](inkword-element.md)zurückgegebene Vertrauenswürdigkeit.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**InkWord**](inkword-element.md)

## <a name="values"></a>Werte

Gültige Werte für dieses Feld sind "0", "1" und "2". 0 weist auf sicheres Vertrauen, 1 auf zwischen Vertrauen und 2 auf ein unsicheres Vertrauen hin.

## <a name="child-elements"></a>Untergeordnete Elemente

Keine

## <a name="attributes"></a>Attribute

Keine

## <a name="element-information"></a>Elementinformationen



|              |                                            |
|--------------|--------------------------------------------|
| Elementtyp | **xs:string**                              |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk |
| Schemaname  | Journal Leser                             |



 

 

 



