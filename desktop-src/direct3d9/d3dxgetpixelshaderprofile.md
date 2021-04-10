---
description: Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: D3DXGetPixelShaderProfile-Funktion (D3DX9Shader. h)
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
ms.openlocfilehash: ad1f430a95b1ff2173dceb1e0561dccf3d0ee88d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961600"
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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das Gerät. Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der HLSL-Profilname.

Wenn das Gerät keine Pixel-Shader unterstützt, gibt die Funktion **null** zurück.

## <a name="remarks"></a>Bemerkungen

Ein Shader-Profil gibt die zu verwendende Assembly-Shader-Version und die Funktionen an, die dem HLSL-Compiler beim Kompilieren eines Shaders zur Verfügung stehen. In der folgenden Tabelle sind die unterstützten Pixel-shaderprofile aufgeführt.



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
<td>Kompilieren Sie in PS_2_0 Version.</td>
</tr>
<tr class="even">
<td>ps_2_a</td>
<td>Identisch mit dem PS_2_0 Profil mit den folgenden zusätzlichen Funktionen, die für den Compiler als Ziel verfügbar sind:
<ul>
<li>Die Anzahl der temporären Register (r #) ist größer als oder gleich 22.</li>
<li>Beliebiger Quellpfad.</li>
<li>Farbverlaufs Anweisungen: DSX, DSY.</li>
<li>Prädikation übersprungen.</li>
<li>Keine abhängige Textur Lese Begrenzung.</li>
<li>Keine Beschränkung für die Anzahl der Textur Anweisungen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>ps_2_b</td>
<td>Identisch mit dem PS_2_0 Profil mit den folgenden zusätzlichen Funktionen, die für den Compiler als Ziel verfügbar sind:
<ul>
<li>Die Anzahl der temporären Register (r #) ist größer als oder gleich 32.</li>
<li>Keine Beschränkung für die Anzahl der Textur Anweisungen.</li>
</ul></td>
</tr>
<tr class="even">
<td>ps_3_0</td>
<td>Kompilieren Sie in ps_3_0 Version.</td>
</tr>
</tbody>
</table>



 

Weitere Informationen zu den Unterschieden zwischen shaderversionen finden Sie [unter Unterschiede bei Pixel-Shadern](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shaderfunktionen](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
