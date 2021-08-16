---
title: Absoluter Wert
description: Verwenden Sie den absoluten Wert eines Quellopernden, der in einer arithmetischen Operation verwendet wird.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 904ff3bb89e71a95a1c88851426ba283987ba6b96f336c91dd443794ee5e143d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795409"
---
# <a name="absolute-value"></a>Absoluter Wert

Verwenden Sie den absoluten Wert eines Quellopernden, der in einer arithmetischen Operation verwendet wird.



| \_Abs |
|-------|



 

Dieser Modifizierer wird nur für Gleitkomma- und Anweisungen mit einfacher und doppelter Genauigkeit verwendet. Der **\_ Abs-Modifizierer** erzwingt das Vorzeichen der Zahl(n) für den Quellopernden positiv, einschließlich der INF-Werte.

Das Anwenden von **\_ abs** auf NaN behält NaN bei, obwohl das jeweilige NaN-Bitmuster, das ergebnisse, nicht definiert ist.

Wenn \_ abs mit dem [Negationmodifizierer](negate.md) kombiniert wird, erzwingt die Kombination, dass das Vorzeichen negativ ist, als ob der **\_ Abs-Modifizierer** zuerst angewendet wird, und dann das **Negieren**.

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Dieser Modifizierer wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungsmodifizierer](instruction-modifiers.md)
</dt> </dl>

 

 




