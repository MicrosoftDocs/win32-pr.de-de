---
description: Gibt einen Ablauf Verfolgungs Anbieter (ETW oder WPP) für MF-Ablauf Verfolgung an.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753897"
---
# <a name="provider-element"></a>provider-Element

Gibt einen Ablauf Verfolgungs Anbieter (ETW oder WPP) für [MF](mftrace.md)-Ablauf Verfolgung an.

## <a name="usage"></a>Verbrauch

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a>Attribute



| Attribut            | type             | Erforderlich       | BESCHREIBUNG                                              |
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
| [**providers**](providers.md)<br/> |



## <a name="element-information"></a>Elementinformationen



|              |     |
|--------------|-----|
| Kann leer bleiben | Nein  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MF-Ablauf Verfolgungs Konfigurationsdatei](mftrace-configuration-file.md)
</dt> </dl>

 

 




