---
description: Sperrt den Gitter Puffer, der die Daten des Mesh-Attributs enthält, und gibt einen Zeiger darauf zurück.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'ID3DXMesh:: LockAttributeBuffer-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 901cb98a9d75d08b6412d6fdca841d403064354b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370410"
---
# <a name="id3dxmeshlockattributebuffer-method"></a>ID3DXMesh:: LockAttributeBuffer-Methode

Sperrt den Gitter Puffer, der die Daten des Mesh-Attributs enthält, und gibt einen Zeiger darauf zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
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

*ppData* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\*\***

Adresse eines Zeigers auf einen Puffer, der ein DWORD für jedes Gesicht im Mesh enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Wenn [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md) aufgerufen wurde, verfügt das Mesh auch über eine Attribut Tabelle, auf die mithilfe der [**ID3DXBaseMesh:: GetAttributeTable**](id3dxbasemesh--getattributetable.md) -Methode zugegriffen werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[**ID3DXBaseMesh:: GetAttributeTable**](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[**ID3DXMesh:: Einstellungs Tabelle**](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
