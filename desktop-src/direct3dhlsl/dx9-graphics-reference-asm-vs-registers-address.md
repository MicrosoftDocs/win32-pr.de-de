---
title: Adress Register
description: Das a0-Register ist ein Adressregister.
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856583"
---
# <a name="address-register"></a>Adress Register

Das a0-Register ist ein Adressregister. Ein einzelnes Register ist in Version vs \_ 1 \_ 1 verfügbar. Das Adressregister, das als a0. x in vs \_ 1 \_ 1 festgelegt ist, kann als Vorzeichen lose Ganzzahl mit Vorzeichen für die relative Adressierung in die Konstante Register Datei verwendet werden. Für Versionen im Vergleich zu \_ 2 \_ 0 und höher sind alle vier Komponenten (x, y,. z,. w) für die relative Adressierung verfügbar.


```
c[a0.x + n]
```



Das Adressregister kann nicht von einem Vertex-Shader gelesen werden, sondern kann nur für die relative Adressierung eines konstanten Registers verwendet werden. Beim Lesen von Werten außerhalb des zulässigen Bereichs wird (0,0, 0,0, 0,0, 0,0) zurückgegeben. Das Adressregister kann nur ein Ziel für die [MOV-vs-](mov---vs.md) Anweisung sein. Wenn eine Gleit Komma Zahl in ein ganzzahliges Register verschoben wird, wird eine roundTo-Next-Konvertierung durchgeführt.

Alle Shader müssen das Adressregister initialisieren, bevor Sie Sie verwenden. Für Version vs \_ 2 \_ 0 und höher kann die [mova-vs-](mova---vs.md) Anweisung einen Gleit Komma Wert in ein Adressregister verschieben.



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Adress Register       | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




