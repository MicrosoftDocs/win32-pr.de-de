---
title: vs
description: Verschieben Sie Daten aus einer Gleit Komma Registrierung in das Adressregister a0.
ms.assetid: 929a0670-f337-4d6d-a7e7-d285e7dc8ae1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ac29bf0d74b4eb2cb6cb86bdf6b070cf56823eb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976473"
---
# <a name="mova---vs"></a>vs

Verschieben Sie Daten aus einer Gleit Komma Registrierung in das [Adressregister](dx9-graphics-reference-asm-vs-registers-address.md)a0.

## <a name="syntax"></a>Syntax



| MUVA DST, src |
|---------------|



 

where

-   DST muss das [Adress Register](dx9-graphics-reference-asm-vs-registers-address.md)(a0) sein.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| der ANWA                   |      | x    | x    | x     | x    | x     |



 

Verschiebt Gleit Komma Daten in ein ganzzahliges Register. Die Werte werden von Gleit Komma Zahlen mit Rundung zum nächsten konvertiert.

Das Adressregister ist das einzige zulässige Ziel Register.

Das folgende Code Fragment zeigt die ausgeführten Vorgänge.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src);
    dest = intSrc;
}
else
{
    dest = src;
}
```



Bei den Versionen 2 \_ x und höher ist das Adressregister ein Komponenten Vektor. Daher ist jede Schreib Maske zulässig.


```
mova a0.xz, r0
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




