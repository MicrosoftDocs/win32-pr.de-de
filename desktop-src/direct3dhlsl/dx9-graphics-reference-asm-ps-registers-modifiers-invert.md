---
title: Quellregister invertiert
description: Führt eine Berechnung (1 – Wert) für jeden Kanal des angegebenen Registers aus.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a391219f085c18a4c8bf2925a248800b6a26838cc6e2b8556551eb98b5335241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562770"
---
# <a name="source-register-invert"></a>Quellregister invertiert

Führt eine Berechnung (1 – Wert) für jeden Kanal des angegebenen Registers aus.

## <a name="syntax"></a>Syntax


```
1 - register
```



## <a name="registers"></a>Register

Quellregister. Weitere Informationen zu Registertypen finden Sie unter [ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Register .](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)

## <a name="remarks"></a>Hinweise

Der Inhalt des Registers wird nicht geändert. Der Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet. Der Invertvorgang wird auf alle vier Farbkanäle (RGBA) angewendet.

Dieser Modifizierer kann nur mit arithmetischen Anweisungen verwendet werden. Darüber hinaus kann dieser Modifizierer nicht mit der anderen [Zielregister-Schreibmaske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)kombiniert werden.

## <a name="example"></a>Beispiel

In diesem Beispiel wird inversion verwendet, um das Komplement des Registers r1 zu generieren.


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellregistermodifizierer für Pixelshader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




