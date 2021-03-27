---
title: Eingabe Register
description: Eingabe Register
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947860"
---
# <a name="input-register"></a>Eingabe Register

Vertex-Shader-Eingabe Register.

Daten aus jedem Scheitelpunkt (mit einem oder mehreren eingegebenen Scheitelpunkt strömen) werden vor dem Ausführen des Vertexshaders in die Scheitelpunkt Eingabe Register geladen. Die Eingabe Register bestehen aus 16 4-Komponenten-Gleit Komma Vektoren, die als v0 bis V15 bezeichnet werden. Diese Register sind schreibgeschützt. Ein Eingabe Register ist über eine Scheitelpunkt Deklaration an Scheitelpunkt Daten gebunden.

Die folgenden Register Eigenschaften steuern, wie sich die einzelnen Register Verhalten:



| Eigenschaft        | BESCHREIBUNG                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| Name            | v \[ n \] -n ist eine optionale Registernummer. 0 ist der Standardwert, der verwendet wird, wenn er weggelassen wird.     |
| Anzahl           | Maximal 16 Register, v0-V15.                                                          |
| E/a-Berechtigungen | Schreibgeschützt. Dieses Register kann nicht von der API oder im Shader geschrieben werden.                   |
| Leseports      | 1. gibt an, wie oft ein Register innerhalb einer einzigen Anweisung gelesen werden kann. Siehe unten. |



 

Jede einzelne Anweisung kann nur auf ein Scheitelpunkt Eingabe Register zugreifen. Allerdings kann jede Quelle in der Anweisung den Vektor beim Lesen unabhängig voneinander verwischen und negieren.

## <a name="example"></a>Beispiel

Es folgt ein Beispiel für die Verwendung einer Scheitelpunkt Deklaration zum Binden von 2D-Scheitelpunkt Positionsdaten an die Registrierung von v0

Die Vertex-Deklaration gehört zu der Anwendung:


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



Im folgenden finden Sie die entsprechende Vertex-Shader-Deklaration:


```
dcl_position v0
```





| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Positions Register      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




