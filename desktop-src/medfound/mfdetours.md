---
description: Gibt den Microsoft Media Foundation Detours-Anbieter an, der Media Foundation API-Aufrufe verfolgt.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: mfdetours-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cd03711c74c21a9a6ff33d2cc2560e4b6d6e0a3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119335"
---
# <a name="mfdetours-element"></a>mfdetours-Element

Gibt den Microsoft Media Foundation Detours-Anbieter an, der Media Foundation API-Aufrufe verfolgt.

## <a name="usage"></a>Verwendung

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a>Attribute



| attribute            | Typ             | Erforderlich       | Beschreibung                             |
|----------------------|------------------|----------------|-----------------------------------------|
| **level**<br/> | CDATA<br/> | Ja<br/> | Die Ablaufverfolgungsebene.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                               |
|---------------------------------------|
| [**Schlüsselwort**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
keyword+
```

## <a name="parent-elements"></a>Übergeordnete Elemente

| Element                                   |
|-------------------------------------------|
| [**Anbieter**](providers.md)<br/> |



## <a name="element-information"></a>Elementinformationen

:::row:::
    :::column:::
        Kann leer bleiben
    :::column-end:::
    :::column span="2":::
        Nein
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MFTrace-Konfigurationsdatei](mftrace-configuration-file.md)
</dt> </dl>

 

 




