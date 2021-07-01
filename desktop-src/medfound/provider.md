---
description: Gibt einen Ablaufverfolgungsanbieter (ETW oder WPP) für MFTrace an.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118445"
---
# <a name="provider-element"></a>provider-Element

Gibt einen Ablaufverfolgungsanbieter (ETW oder WPP) für [MFTrace](mftrace.md)an.

## <a name="usage"></a>Verwendung

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a>Attribute



| attribute            | Typ             | Erforderlich       | BESCHREIBUNG                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| **ID**<br/>    | CDATA<br/> | Ja<br/> | Der Name oder die GUID des Anbieters.<br/> <br/> |
| **level**<br/> | CDATA<br/> | Ja<br/> | Die Ablaufverfolgungsebene.<br/> <br/>                  |



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

 

 




