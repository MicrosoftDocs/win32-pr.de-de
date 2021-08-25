---
description: Konvertiert die angegebene Gitternetzteilmenge in einen einzelnen Dreiecksstreifen.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: D3DXConvertMeshSubsetToSingleStrip-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToSingleStrip
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53d3ec4a0362ec923fdbeaa1d880188039e866292897d3fe5518ae34d4e2622d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857370"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a>D3DXConvertMeshSubsetToSingleStrip-Funktion

Konvertiert die angegebene Gitternetzteilmenge in einen einzelnen Dreiecksstreifen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MeshIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Zeiger auf eine [**ID3DXBaseMesh-Schnittstelle,**](id3dxbasemesh.md) die das Gitternetz darstellt, das in einen Strip konvertiert werden soll.

</dd> <dt>

*AttribId* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Attribut-ID der Gitternetzteilmenge, die in Strips konvertiert werden soll.

</dd> <dt>

*IBOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren Flags aus der [**D3DXMESH-Enumeration,**](./d3dxmesh.md) die Optionen zum Erstellen des Indexpuffers angeben. D3DXMESH \_ kann nicht 32 BIT sein. Der Indexpuffer wird mit 32-Bit- oder 16-Bit-Indizes erstellt, abhängig vom Format des Indexpuffers des Gitternetzes, das durch den *MeshIn-Parameter* angegeben wird.

</dd> <dt>

*ppIndexBuffer* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Zeiger auf eine [**IDirect3DIndexBuffer9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) die den Indexpuffer darstellt, der den Strip enthält.

</dd> <dt>

*pNumIndices* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Anzahl der Indizes im Puffer, die im *ppIndexBuffer-Parameter* zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Rufen Sie vor dem Ausführen dieser Funktion [**Optimize**](id3dxmesh--optimize.md) oder [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)auf, wobei das D3DXMESHOPT \_ ATTRSORT-Flag festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
