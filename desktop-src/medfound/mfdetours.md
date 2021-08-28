---
description: Gibt den Microsoft Media Foundation Detours-Anbieter an, der Media Foundation API-Aufrufe verfolgt.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: mfdetours-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a0215d9d065bd27f0ad98ebea23abec8f7ecbbfc2223d522e0ddd1887990c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113640"
---
# <a name="mfdetours-element"></a>mfdetours-Element

Gibt den Microsoft Media Foundation Detours-Anbieter an, der Media Foundation API-Aufrufe verfolgt.

## <a name="usage"></a>Verbrauch

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a>Attribute



| attribute            | type             | Erforderlich       | Beschreibung                             |
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

 

 




