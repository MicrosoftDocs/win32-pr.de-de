---
title: Eingaberegister
description: Eingaberegister
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6682d8987f2df3ba3fb06427d41b722abb5eb003a4226a155c104cc3239d0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982760"
---
# <a name="input-register"></a>Eingaberegister

Vertex-Shader-Eingaberegister.

Daten von jedem Scheitelpunkt (mit einem oder mehreren Eingabevertexstreams) werden in die Vertexeingaberegister geladen, bevor der Vertex-Shader ausgeführt wird. Die Eingaberegister bestehen aus 16 Gleitkommavektoren mit vier Komponenten, die als v0 bis v15 festgelegt sind. Diese Register sind schreibgeschützt. Ein Eingaberegister wird über eine Scheitelpunktdeklaration an Scheitelpunktdaten gebunden.

Die folgenden Registereigenschaften steuern, wie sich jedes Register verhält:



| Eigenschaft        | BESCHREIBUNG                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| Name            | v \[ n \] - n ist eine optionale Registernummer. 0 ist der standardwert, der verwendet wird, wenn er ausgelassen wird.     |
| Anzahl           | Maximal 16 Register, v0 – v15.                                                          |
| E/A-Berechtigungen | Schreibgeschützt. Dieses Register kann nicht von der API oder innerhalb des Shaders geschrieben werden.                   |
| Leseports      | 1. Dies ist die Anzahl, mit der ein Register innerhalb einer einzelnen Anweisung gelesen werden kann. Siehe unten. |



 

Jede einzelne Anweisung kann nur auf ein Scheitelpunkteingaberegister zugreifen. Jede Quelle in der Anweisung kann jedoch unabhängig voneinander wischen und diesen Vektor beim Lesen negieren.

## <a name="example"></a>Beispiel

Hier ist ein Beispiel für die Verwendung einer Scheitelpunktdeklaration zum Binden von 2D-Scheitelpunktpositionsdaten zum Registrieren von v0.

Die Scheitelpunktdeklaration gehört zur Anwendung:


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



Hier ist die entsprechende Vertex-Shaderdeklaration:


```
dcl_position v0
```





| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Positionsregister      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




