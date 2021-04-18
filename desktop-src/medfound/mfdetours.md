---
description: Gibt den Microsoft Media Foundation umleitet-Anbieter an, der Media Foundation API-Aufrufe verfolgt.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: MF-Umleitungen-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09d39d6f8a7c7ff1d88471e71c6fc58aa49bd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343736"
---
# <a name="mfdetours-element"></a>MF-Umleitungen-Element

Gibt den Microsoft Media Foundation umleitet-Anbieter an, der Media Foundation API-Aufrufe verfolgt.

## <a name="usage"></a>Verbrauch

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a>Attribute



| Attribut            | type             | Erforderlich       | BESCHREIBUNG                             |
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
| [**providers**](providers.md)<br/> |



## <a name="element-information"></a>Elementinformationen



|              |     |
|--------------|-----|
| Kann leer bleiben | Nein  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MF-Ablauf Verfolgungs Konfigurationsdatei](mftrace-configuration-file.md)
</dt> </dl>

 

 




