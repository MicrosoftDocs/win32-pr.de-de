---
title: Textur-Typ
description: Verwenden Sie die folgende Syntax, um eine Textur Variable zu deklarieren.
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- Textur Type HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2020
ms.locfileid: "103723984"
---
# <a name="texture-type"></a>Textur-Typ

Verwenden Sie die folgende Syntax, um eine Textur Variable zu deklarieren.

|                |
|----------------|
| **Typname;** |

## <a name="parameters"></a>Parameter
| Element                                                                                     | BESCHREIBUNG                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Sorte**<br/> | Einer der folgenden Typen: Textur (nicht typisiert, aus Gründen der Abwärtskompatibilität), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, texturecube. Die Elementgröße muss in 4 32-Bit-Mengen passen.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**<br/> | Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.<br/>                                                                                                                                                   |
## <a name="remarks"></a>Bemerkungen

Die Verwendung einer Textur besteht aus drei Teilen.

1.  Deklarieren einer Textur Variablen. Dies erfolgt mit der oben gezeigten Syntax. Dies sind z. b. gültige Deklarationen.

    ```
    texture g_MeshTexture;
    ```

    \- oder -

    ```
    Texture2D g_MeshTexture;
    ```

2.  Deklarieren und Initialisieren eines samplerobjekts. Dies erfolgt mit einer etwas anderen Syntax in Direct3D 9 und Direct3D 10. Ausführliche Informationen zur samplerobjektsyntax finden Sie unter [Sampler-Typ (DirectX HLSL)](dx-graphics-hlsl-sampler.md).
3.  Aufrufen einer Textur Funktion in einem Shader.

Unterschiede zwischen Direct3D 9 und Direct3D 10:

Direct3D 9 verwendet systeminterne [Textur Funktionen](dx-graphics-hlsl-intrinsic-functions.md) , um Textur Operationen auszuführen. Dieses Beispiel basiert auf dem [basichlsl](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) -Beispiel und verwendet [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) zum Durchführen von Textur Stichproben.

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

Direct3D 10 verwendet stattdessen vorlagenbasierte [Textur Objekte](dx-graphics-hlsl-to-type.md) . Im folgenden finden Sie ein Beispiel für die äquivalente Textur Operation.

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a>Weitere Informationen

[Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
