---
description: Sperrt einen Scheitelpunkt Puffer und erhält einen Zeiger auf den Vertex-Pufferspeicher.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'ID3DXBaseMesh:: lockvertexbuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e93e59715d9f262d7693f2bef652f8be63337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357240"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a>ID3DXBaseMesh:: lockvertexbuffer-Methode

Sperrt einen Scheitelpunkt Puffer und erhält einen Zeiger auf den Vertex-Pufferspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination von 0 (null) oder mehreren Sperr Flags, die den Typ der auszuführenden Sperre beschreiben. Für diese Methode sind die gültigen Flags:

-   D3DLOCK \_ verwerfen
-   D3DLOCK \_ kein \_ Dirty \_ Update
-   D3DLOCK \_ nosyslock
-   D3DLOCK \_ schreibgeschützt
-   D3DLOCK \_ noüberschreibung

Eine Beschreibung der Flags finden Sie unter [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ Out, retval\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***

VOID- \* Zeiger auf einen Puffer, der die Scheitelpunkt Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Wenn Sie mit Scheitelpunkt Puffern arbeiten, können Sie mehrere Sperr Aufrufe durchführen. Sie müssen jedoch sicherstellen, dass die Anzahl der Sperr Aufrufe mit der Anzahl der entsperrungs Aufrufe identisch ist. Bei drawprimitive-aufrufen gibt es keine ausstehenden Sperr Zähler für einen aktuell festgelegten Scheitelpunkt Puffer.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
