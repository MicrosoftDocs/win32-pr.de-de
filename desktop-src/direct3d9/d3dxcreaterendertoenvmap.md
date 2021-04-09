---
description: Erstellt eine Rendering-Umgebungs Zuordnung.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: D3DXCreateRenderToEnvMap-Funktion (D3dx9core. h)
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
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050856"
---
# <a name="d3dxcreaterendertoenvmap-function"></a>D3DXCreateRenderToEnvMap-Funktion

Erstellt eine Rendering-Umgebungs Zuordnung.

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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät ist, das der Renderoberfläche zugeordnet werden soll.

</dd> <dt>

*Größe* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Größe der Renderoberfläche.

</dd> <dt>

*Miplevels* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl von MipMap-Ebenen.

</dd> <dt>

*Format* \[ in\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Pixel Format der Umgebungs Zuordnung beschreibt.

</dd> <dt>

*Depthstencil* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

**True** gibt an, dass die Renderoberfläche eine tiefen Schablone unterstützt. Andernfalls ist dieser Member auf **false** festgelegt.

</dd> <dt>

*Depthstencilformat* \[ in\]
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

Wenn depthstencil auf **true** festgelegt ist, ist dieser Parameter ein Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das tiefen Schablone-Format der Umgebungs Zuordnung beschreibt.

</dd> <dt>

*pprenderumenvmap* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***

Adresse eines Zeigers auf eine [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) -Schnittstelle, die die erstellte Rendering-Umgebungs Zuordnung darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
