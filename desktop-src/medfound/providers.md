---
description: Enthält eine Liste der Ablauf Verfolgungs Anbieter für MF Trace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: providers-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215016"
---
# <a name="providers-element"></a>providers-Element

Enthält eine Liste der Ablauf Verfolgungs Anbieter für [MF Trace](mftrace.md).

## <a name="usage"></a>Verbrauch

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**MF-Umleitungen**](mfdetours.md)<br/> | Gibt den Media Foundation umleitet-Anbieter an, der Media Foundation API-Aufrufe verfolgt.<br/> <br/> |
| [**ab**](provider.md)<br/>   | Gibt einen Ablauf Verfolgungs Anbieter (ETW oder WPP) an.<br/> <br/>                                                  |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente

Es gibt keine übergeordneten Elemente.

## <a name="element-information"></a>Elementinformationen



|              |     |
|--------------|-----|
| Kann leer bleiben | Ja |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MF-Ablauf Verfolgungs Konfigurationsdatei](mftrace-configuration-file.md)
</dt> </dl>

 

 




