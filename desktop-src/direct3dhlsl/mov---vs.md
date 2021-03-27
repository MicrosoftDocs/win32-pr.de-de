---
title: MOV (VS)
description: Verschieben von Gleit Komma Daten zwischen Registern.
ms.assetid: bf013ab2-593e-4201-ba75-faebd0c9f97a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00f207261ad8ba6ac83360c40bc6008530292816
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719452"
---
# <a name="mov---vs"></a>MOV (VS)

Verschieben von Gleit Komma Daten zwischen Registern.

## <a name="syntax"></a>Syntax



| MOV DST, src |
|--------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| MOV                    | x    | x    | x    | x     | x    | x     |



 

Kann für Gleit Komma Daten verwendet werden. Für Version vs \_ 1 \_ 1 kann Sie auch verwendet werden, um das Adressregister zu schreiben. Wenn Sie zum Aktualisieren von Adress Registern verwendet werden, werden die Werte von Gleit Komma Zahlen mithilfe der Rundung zum nächsten konvertiert.

Das folgende Code Fragment zeigt die ausgeführten Vorgänge.


```
if(dest is an integer register)
{
    int intSrc = RoundToNearest(src.w);
    dest = intSrc;
}
else
{
    dest = src;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




