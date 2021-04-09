---
description: Sperrt einen Index Puffer und erhält einen Zeiger auf den Speicher des Index Puffers.
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: 'ID3DXBaseMesh:: LockIndexBuffer-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 388915d0d11ff910c19a2c70b305597a79cd04bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050832"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a>ID3DXBaseMesh:: LockIndexBuffer-Methode

Sperrt einen Index Puffer und erhält einen Zeiger auf den Speicher des Index Puffers.

## <a name="syntax"></a>Syntax


```C++
HRESULT LockIndexBuffer(
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

Eine Beschreibung der Flags finden Sie unter [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ Out, retval\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***

VOID- \* Zeiger auf einen Puffer, der die Indexdaten enthält. Die Anzahl der Indizes in diesem Puffer ist gleich [**ID3DXBaseMesh:: getnumgesichter**](id3dxbasemesh--getnumfaces.md) \* 3.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Beim Arbeiten mit Index Puffern können Sie mehrere Sperr Aufrufe durchführen. Sie müssen jedoch sicherstellen, dass die Anzahl der Sperr Aufrufe mit der Anzahl der entsperrungs Aufrufe identisch ist. Drawprimitive-Aufrufe können nicht mit einer ausstehenden Sperr Anzahl für einen aktuell festgelegten Index Puffer ausgeführt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
