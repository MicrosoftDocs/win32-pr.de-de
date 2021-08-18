---
description: Sperrt einen Scheitelpunktpuffer und ruft einen Zeiger auf den Vertexpufferspeicher ab.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: ID3DXBaseMesh::LockVertexBuffer-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: 5bb0cd8539a996b66ccf9f413e57ebf1d213fe6372e56b50b35abc5e210595f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987610"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a>ID3DXBaseMesh::LockVertexBuffer-Methode

Sperrt einen Scheitelpunktpuffer und ruft einen Zeiger auf den Vertexpufferspeicher ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination von null oder mehr Sperrflags, die den Typ der auszuführenden Sperre beschreiben. Für diese Methode sind die gültigen Flags:

-   D3DLOCK \_ DISCARD
-   D3DLOCK \_ KEIN \_ GEÄNDERTES \_ UPDATE
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ READONLY
-   D3DLOCK \_ NOOVERWRITE

Eine Beschreibung der Flags finden Sie unter [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*VOID-Zeiger auf einen Puffer, der die Scheitelpunktdaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Wenn Sie mit Scheitelpunktpuffern arbeiten, können Sie mehrere Sperraufrufe vornehmen. Sie müssen jedoch sicherstellen, dass die Anzahl der Sperraufrufe mit der Anzahl der Entsperraufrufe übereinstimmt. DrawPrimitive-Aufrufe sind mit einer ausstehenden Sperranzahl für einen derzeit festgelegten Scheitelpunktpuffer nicht erfolgreich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
