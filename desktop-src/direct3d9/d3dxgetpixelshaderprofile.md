---
description: 'D3DXGetPixelShaderProfile-Funktion: Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.'
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: D3DXGetPixelShaderProfile-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d24e19d49a8a96f91847892f519ef6c06d25ef5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114437"
---
# <a name="d3dxgetpixelshaderprofile-function"></a>D3DXGetPixelShaderProfile-Funktion

Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das Gerät. Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der HLSL-Profilname.

Wenn das Gerät keine Pixelshader unterstützt, gibt die Funktion **NULL** zurück.

## <a name="remarks"></a>Bemerkungen

Ein Shaderprofil gibt die zu verwendende Assembly-Shaderversion und die Funktionen an, die dem HLSL-Compiler beim Kompilieren eines Shaders zur Verfügung stehen. In der folgenden Tabelle sind die unterstützten Pixel-Shaderprofile aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Shaderprofil</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ps_1_1</td>
<td>Kompilieren Sie in ps_1_1 Version.</td>
</tr>
<tr class="even">
<td>ps_1_2</td>
<td>Kompilieren Sie in ps_1_2 Version.</td>
</tr>
<tr class="odd">
<td>ps_1_3</td>
<td>Kompilieren Sie in ps_1_3 Version.</td>
</tr>
<tr class="even">
<td>ps_1_4</td>
<td>Kompilieren Sie in ps_1_4 Version.</td>
</tr>
<tr class="odd">
<td>ps_2_0</td>
<td>Kompilieren Sie in ps_2_0 Version.</td>
</tr>
<tr class="even">
<td>ps_2_a</td>
<td>Entspricht dem ps_2_0 Profil mit den folgenden zusätzlichen Funktionen, die der Compiler als Ziel hat:
<ul>
<li>Die Anzahl temporärer Register (r#) ist größer oder gleich 22.</li>
<li>Beliebige Quellwizzle.</li>
<li>Farbverlaufsanweisungen: dsx, dsy.</li>
<li>Prädikation:</li>
<li>Kein Leselimit für abhängige Textur.</li>
<li>Keine Beschränkung für die Anzahl der Texturanweisungen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>ps_2_b</td>
<td>Entspricht dem ps_2_0 Profil mit den folgenden zusätzlichen Funktionen, die der Compiler als Ziel hat:
<ul>
<li>Die Anzahl temporärer Register (r#) ist größer oder gleich 32.</li>
<li>Keine Beschränkung für die Anzahl der Texturanweisungen.</li>
</ul></td>
</tr>
<tr class="even">
<td>ps_3_0</td>
<td>Kompilieren Sie in ps_3_0 Version.</td>
</tr>
</tbody>
</table>



 

Weitere Informationen zu den Unterschieden zwischen Shaderversionen finden Sie unter [Pixelshader-Unterschiede.](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
