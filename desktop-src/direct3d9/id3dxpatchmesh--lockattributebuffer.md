---
description: Sperrt den Attribut Puffer.
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: 'ID3DXPatchMesh:: LockAttributeBuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71e50fdc27f3f50b560324c74f5a1609f900772d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367502"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a>ID3DXPatchMesh:: LockAttributeBuffer-Methode

Sperrt den Attribut Puffer.

## <a name="syntax"></a>Syntax


```C++
HRESULT LockAttributeBuffer(
  [in]          DWORD flags,
  [out, retval] DWORD **ppData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination von 0 (null) oder mehreren Sperr Flags, die den Typ der auszuführenden Sperre beschreiben. Für diese Methode sind die gültigen Flags:

-   D3DLOCK \_ verwerfen
-   D3DLOCK \_ kein \_ Dirty \_ Update
-   D3DLOCK \_ nosyslock
-   D3DLOCK \_ schreibgeschützt

Eine Beschreibung der Flags finden Sie unter [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ Out, retval\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\*\***

Adresse eines Zeigers auf einen Puffer, der ein DWORD für jedes Gesicht im Mesh enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Der Attribut Puffer ist in der Regel gesperrt, in geschrieben und dann zum Lesen entsperrt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
