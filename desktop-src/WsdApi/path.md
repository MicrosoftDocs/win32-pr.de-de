---
description: Gibt den Speicherort und den Dateinamen einer WSDL-Datei an. Der Pfad kann ein absoluter oder relativer Pfad zur Datei sein, darf jedoch keine URL sein.
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: path-Element (Webdienste auf Geräten)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48df5a156149f00b8b153ccc0d46d6d2d34a1ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994307"
---
# <a name="path-element"></a>path-Element

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
| [**Wsdl**](wsdl.md)<br/> | Eine WSDL-Datei, die für Vertragsinformationen verarbeitet werden soll.<br/> <br/> |



## <a name="examples"></a>Beispiele

Der folgende XML-Code zeigt ein gültiges **Pfadelement.**

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




