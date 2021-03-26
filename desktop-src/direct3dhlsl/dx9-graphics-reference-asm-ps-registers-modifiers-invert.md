---
title: Quell Register Invert
description: Führt für jeden Kanal des angegebenen Register eine (1-Wert)-Berechnung aus.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976168"
---
# <a name="source-register-invert"></a>Quell Register Invert

Führt für jeden Kanal des angegebenen Register eine (1-Wert)-Berechnung aus.

## <a name="syntax"></a>Syntax


```
1 - register
```



## <a name="registers"></a>Register

Quell Register. Weitere Informationen zu Register Typen finden Sie unter [PS \_ 1 1 PS 1 \_ \_ \_ \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Bemerkungen

Der Inhalt des Registers wird nicht geändert. Der-Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet. Der umkehren-Vorgang wird auf alle vier Farbkanäle (RGBA) angewendet.

Dieser Modifizierer kann nur mit arithmetischen Anweisungen verwendet werden. Außerdem kann dieser Modifizierer nicht mit der anderen Ziel- [Schreib Maske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)für das Schreiben kombiniert werden.

## <a name="example"></a>Beispiel

In diesem Beispiel wird Inversion verwendet, um das Komplement von Register R1 zu generieren.


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader-quellregistrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




