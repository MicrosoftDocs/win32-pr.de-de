---
description: Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: D3DXGetVertexShaderProfile-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f7ccaeba60bdd1d7c512cee3fb4da29289408a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353722"
---
# <a name="d3dxgetvertexshaderprofile-function"></a>D3DXGetVertexShaderProfile-Funktion

Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das Gerät. Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der HLSL-Profilname.

Wenn das Gerät Scheitelpunkt-Shader nicht unterstützt, gibt die Funktion **null** zurück.

## <a name="remarks"></a>Bemerkungen

Ein Shader-Profil gibt die zu verwendende Assembly-Shader-Version und die Funktionen an, die dem HLSL-Compiler beim Kompilieren eines Shaders zur Verfügung stehen. In der folgenden Tabelle sind die unterstützten Vertex-shaderprofile aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Shader-Profil</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vs_1_1</td>
<td>Kompilieren Sie in vs_1_1 Version.</td>
</tr>
<tr class="even">
<td>vs_2_0</td>
<td>Kompilieren Sie in VS_2_0 Version.</td>
</tr>
<tr class="odd">
<td>vs_2_a</td>
<td>Identisch mit dem VS_2_0 Profil mit den folgenden zusätzlichen Funktionen, die für den Compiler als Ziel verfügbar sind:
<ul>
<li>Die Anzahl der temporären Register (r #) ist größer als oder gleich 13.</li>
<li>Dynamische Fluss Steuerungs Anweisung.</li>
<li>Prädikation übersprungen.</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_3_0</td>
<td>Kompilieren Sie in vs_3_0 Version.</td>
</tr>
</tbody>
</table>



 

Weitere Informationen zu den Unterschieden zwischen shaderversionen finden Sie [unter Unterschiede im Scheitelpunkt-Shader](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
