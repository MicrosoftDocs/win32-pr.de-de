---
description: Erstellt eine Renderumgebungszuordnung.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: D3DXCreateRenderToEnvMap-Funktion (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f248f70daf589d562091f2bcc235539726b53c8f301d2f10193b13e8604fe740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732274"
---
# <a name="d3dxcreaterendertoenvmap-function"></a>D3DXCreateRenderToEnvMap-Funktion

Erstellt eine Renderumgebungszuordnung.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät ist, das der Renderoberfläche zugeordnet werden soll.

</dd> <dt>

*Größe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Größe der Renderoberfläche.

</dd> <dt>

*MipLevels* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Mipmapebenen.

</dd> <dt>

*Formatieren* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT-Enumerationstyps,](d3dformat.md) der das Pixelformat der Umgebungszuordnung beschreibt.

</dd> <dt>

*Tiefenschablone* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

**True** gibt an, dass die Renderoberfläche eine Tiefenschablonenoberfläche unterstützt. Andernfalls wird dieser Member auf **FALSE** festgelegt.

</dd> <dt>

*DepthStencilFormat* \[ In\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Wenn DepthStencil auf **TRUE** festgelegt ist, ist dieser Parameter ein Member des [D3DFORMAT-Enumerationstyps,](d3dformat.md) der das Tiefenschablonenformat der Umgebungszuordnung beschreibt.

</dd> <dt>

*ppRenderToEnvMap* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***

Adresse eines Zeigers auf eine [**ID3DXRenderToEnvMap-Schnittstelle,**](id3dxrendertoenvmap.md) die die erstellte Renderumgebungszuordnung darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
