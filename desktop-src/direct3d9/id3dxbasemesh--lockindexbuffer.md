---
description: Sperrt einen Indexpuffer und erhält einen Zeiger auf den Indexpufferspeicher.
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: ID3DXBaseMesh::LockIndexBuffer-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c2eab2806775572cb4e4c4a50899d48263c6ddf0d55138c37bcaff8367225c3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118820"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a>ID3DXBaseMesh::LockIndexBuffer-Methode

Sperrt einen Indexpuffer und erhält einen Zeiger auf den Indexpufferspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination von null oder mehr Sperrflags, die den Typ der durchzuführenden Sperre beschreiben. Für diese Methode sind die gültigen Flags:

-   D3DLOCK \_ DISCARD
-   D3DLOCK \_ KEIN \_ GEÄNDERTES \_ UPDATE
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ READONLY

Eine Beschreibung der Flags finden Sie unter [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*VOID-Zeiger auf einen Puffer, der die Indexdaten enthält. Die Anzahl der Indizes in diesem Puffer entspricht [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Wenn Sie mit Indexpuffern arbeiten, können Sie mehrere Sperraufrufe tätigen. Sie müssen jedoch sicherstellen, dass die Anzahl der Sperraufrufe mit der Anzahl der Entsperraufrufe übereinstimmen. DrawPrimitive-Aufrufe sind mit ausstehender Sperranzahl für einen aktuell festgelegten Indexpuffer nicht erfolgreich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
