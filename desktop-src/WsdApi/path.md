---
description: Gibt den Speicherort und den Dateinamen einer WSDL-Datei an. Der Pfad kann ein absoluter oder relativer Pfad zur Datei sein, darf jedoch keine URL sein.
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: Path-Element (Webdienste auf Geräten)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 763ad1479c20553fb7e62ab29e504d56bfa6d950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362254"
---
# <a name="path-element"></a>Path-Element

Gibt den Speicherort und den Dateinamen einer WSDL-Datei an. Der Pfad kann ein absoluter oder relativer Pfad zur Datei sein, darf jedoch keine URL sein.

## <a name="usage"></a>Verbrauch

``` syntax
<path/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                             |
|---------------------------------|-------------------------------------------------------------------------|
| [**WSDL**](wsdl.md)<br/> | Eine WSDL-Datei, die für Vertragsinformationen verarbeitet werden soll.<br/> <br/> |



## <a name="examples"></a>Beispiele

Der folgende XML-Code zeigt ein gültiges **path** -Element.

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




