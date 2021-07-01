---
description: Enthält eine Liste der Ablaufverfolgungsanbieter für MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: providers-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38a86bf3ca8ffa1ea9e3da20e0244e7abec8513
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118485"
---
# <a name="providers-element"></a>providers-Element

Enthält eine Liste der Ablaufverfolgungsanbieter für [MFTrace.](mftrace.md)

## <a name="usage"></a>Verwendung

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | Beschreibung                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> | Gibt den Media Foundation Detours-Anbieter an, der Media Foundation API-Aufrufe verfolgt.<br/> <br/> |
| [**Anbieter**](provider.md)<br/>   | Gibt einen Ablaufverfolgungsanbieter (ETW oder WPP) an.<br/> <br/>                                                  |



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

:::row:::
    :::column:::
        Kann leer bleiben
    :::column-end:::
    :::column span="2":::
        Ja
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MFTrace-Konfigurationsdatei](mftrace-configuration-file.md)
</dt> </dl>

 

 




