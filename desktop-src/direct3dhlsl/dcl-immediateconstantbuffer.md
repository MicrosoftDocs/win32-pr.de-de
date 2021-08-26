---
title: dcl_immediateConstantBuffer (sm4 – asm)
description: dcl \_ immediateConstantBuffer (sm4 – asm)
ms.assetid: 55e21ab1-0749-4200-8e68-bb098e935dac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 781a792257b23a3d89cfa432ccc1ead9e5d756159beb428defc3404ba32df47c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024800"
---
# <a name="dcl_immediateconstantbuffer-sm4---asm"></a>dcl \_ immediateConstantBuffer (sm4 – asm)

Deklariert einen Direktkonstantenpuffer eines Shaders.



| dcl \_ *immediateConstantBuffer-Wert(e)* |
|-----------------------------------------|



 

<dl> <dt>

<span id="value_s_"></span><span id="VALUE_S_"></span>*value(s)*
</dt> <dd>

\[in \] Der Puffer darf mindestens einen Wert enthalten, jedoch nicht mehr als 4096 Werte.

</dd> </dl>

### <a name="remarks"></a>Hinweise

Ein Shader ist für einen Unmittelbarkonstantenpuffer zulässig. Auf einen Unmittelbarkonstantenpuffer wird genau wie auf einen konstanten Puffer mit dynamischer Indizierung zugegriffen.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Sie können keinen Shader in der Assemblysprache mit shader Model 4 erstellen.

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




