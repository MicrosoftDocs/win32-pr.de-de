---
title: Quellen Register Negate
description: Führt für alle Register Komponenten eine Negation (y-x) aus.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036852"
---
# <a name="source-register-negate"></a>Quellen Register Negate

Führt für alle Register Komponenten eine Negation (y =-x) aus.

## <a name="syntax"></a>Syntax


```
- register
```



## <a name="registers"></a>Register

Quell Register. Weitere Informationen zu Register Typen finden Sie unter [PS \_ 1 1 PS 1 \_ \_ \_ \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Bemerkungen

Der Inhalt des Registers wird nicht geändert. Der-Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet. Der Negation-Vorgang wird auf alle vier Farbkanäle (RGBA) angewendet.

Dieser Vorgang wird ausgeführt, nachdem alle anderen Modifizierer für dasselbe Argument vorhanden sind.

Dieser Modifizierer schließt sich mit dem [Quell Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) gegenseitig aus, sodass er nicht auf dasselbe Register angewendet werden kann.

Dieser Modifizierer kann nur mit arithmetischen Anweisungen verwendet werden.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird gezeigt, wie dieser Modifizierer verwendet wird.


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel-Shader-quellregistrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




