---
description: Gibt den Speicherort und den Dateinamen einer WSDL-Datei an. Der Pfad kann ein absoluter oder relativer Pfad zur Datei sein, darf jedoch keine URL sein.
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: path-Element (Webdienste auf Geräten)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3597248a2cbead5afdeb2fd1cd41613e1c4617b7be1ea636abb3ddbd2cdc92be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071420"
---
# <a name="path-element"></a>path-Element

Gibt den Speicherort und den Dateinamen einer WSDL-Datei an. Der Pfad kann ein absoluter oder relativer Pfad zur Datei sein, darf jedoch keine URL sein.

## <a name="usage"></a>Verwendung

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



 

 




