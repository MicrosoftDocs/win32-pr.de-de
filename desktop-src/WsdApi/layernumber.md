---
description: Definiert die Anzahl der zu erstellenden Codeebenen.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: layerNumber-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c33ee4468ab81f030bfd8b49dfe104bbe76248
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995487"
---
# <a name="layernumber-element"></a>layerNumber-Element

Definiert die Anzahl der zu erstellenden Codeebenen.

## <a name="usage"></a>Verbrauch

``` syntax
<layerNumber/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer XML-Skriptdatei des WSDAPI-Codegenerators.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Ebenennummern werden in Laufzeittabellen verwendet, um eine Codeebene für eine andere zu unterscheiden. WSDAPI selbst verwendet generierten Code mit der Ebenennummer 0.

In der Regel ist dieser Wert 1, was angibt, dass der generierte Code über WSDAPI und keiner anderen Ebene liegt. In einigen Fällen können höhere Zahlen verwendet werden. Wenn beispielsweise ein Unternehmen Code für eine Geräteklasse (nummerierte Ebene 1) erzeugt, möchte ein bestimmter Hardwareanbieter möglicherweise eine zusätzliche ebene nummerierte Ebene 2 hinzufügen.

Rechtliche Werte, mit Ausnahme von WSDAPI selbst, sind größer als 0 und kleiner als 16.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




