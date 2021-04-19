---
description: Konvertiert die angegebene Gitter Teilmenge in einen einzelnen Dreieck Streifen.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: D3DXConvertMeshSubsetToSingleStrip-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: c76aa52b08a21faf9bc2a6ef35745513063cc3b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357230"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a>D3DXConvertMeshSubsetToSingleStrip-Funktion

Konvertiert die angegebene Gitter Teilmenge in einen einzelnen Dreieck Streifen.

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

*Mesda* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Zeiger auf eine [**ID3DXBaseMesh**](id3dxbasemesh.md) -Schnittstelle, die das Mesh darstellt, das in einen Strip konvertiert werden soll.

</dd> <dt>

*Atungbid* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Attribut-ID der Mesh-Teilmenge, die in Striche konvertiert werden soll.

</dd> <dt>

*Iboptions* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Optionen zum Erstellen des Index Puffers angeben. Darf nicht D3DXMESH \_ 32 Bit sein. Der Index Puffer wird mit 32-Bit-oder 16-Bit-Indizes erstellt, abhängig vom Format des Index Puffers des Netzes, das durch den *mesda* -Parameter angegeben wird.

</dd> <dt>

*ppindexbuffer* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Ein Zeiger auf eine [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) -Schnittstelle, die den Index Puffer darstellt, der den Strip enthält.

</dd> <dt>

*pnumindizes* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Anzahl der Indizes im Puffer, die im *ppindexbuffer* -Parameter zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Stellen Sie vor dem Ausführen dieser Funktion " [**optimieren**](id3dxmesh--optimize.md) " oder " [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)" mit dem D3DXMESHOPT \_ attrsort-Flag her.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
