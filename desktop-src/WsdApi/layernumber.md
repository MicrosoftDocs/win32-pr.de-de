---
description: Definiert die Anzahl der zu generierenden Code Schicht.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: layernumber-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c22a20db7817e449b05c943c9016b6002f35b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216311"
---
# <a name="layernumber-element"></a>layernumber-Element

Definiert die Anzahl der zu generierenden Code Schicht.

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
| [**wsdcodegen**](wsdcodegen.md)<br/> | Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Ebenennummern werden in Lauf Zeit Tabellen verwendet, um eine Codeebene für eine andere zu unterscheiden. WSDAPI selbst verwendet generierten Code mit einer Ebenennummer von 0.

Normalerweise ist dieser Wert 1, was darauf hinweist, dass der generierte Code über WSDAPI und keine andere Ebene geschichtet ist. In einigen Fällen können höhere Zahlen verwendet werden. Wenn ein Unternehmen z. b. Code für eine Geräteklasse (nummerierte Schicht 1) erstellt, möchte ein bestimmter Hardwarehersteller möglicherweise eine weitere Ebene mit der nummerierten Ebene 2 hinzufügen.

Zulässige Werte, außer im Fall von WSDAPI, sind größer als 0 und kleiner als 16.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




