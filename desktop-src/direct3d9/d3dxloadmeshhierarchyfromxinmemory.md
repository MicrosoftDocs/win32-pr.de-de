---
description: Lädt die erste Frame Hierarchie aus einer x-Datei.
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: D3DXLoadMeshHierarchyFromXInMemory-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91cf119fc8907701f87ebb5bda1bb0bf45294aba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371946"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a>D3DXLoadMeshHierarchyFromXInMemory-Funktion

Lädt die erste Frame Hierarchie aus einer x-Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmemory* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Zeiger auf einen Puffer, der die Mesh-Hierarchie enthält.

</dd> <dt>

*Sizeofmemory* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Größe des pmemory-Puffers in Bytes.

</dd> <dt>

*MeshOptions* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Erstellungs Optionen für das Mesh angeben.

</dd> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das dem Mesh zugeordnete Geräte Objekt.

</dd> <dt>

*palloc* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Zeiger auf eine [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) -Schnittstelle.

</dd> <dt>

*puserdataloader* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Von der Anwendung bereitgestellte Schnittstelle, die das Laden von Benutzerdaten ermöglicht Siehe [**ID3DXLoadUserData**](id3dxloaduserdata.md).

</dd> <dt>

*ppframeheirarerig* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)\***

Gibt einen Zeiger auf die geladene Frame Hierarchie zurück. Siehe [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*ppanimcontroller* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Gibt einen Zeiger auf den Animations Controller zurück, der der Animation in der x-Datei entspricht. Dies wird mit Standardspuren und-Ereignissen erstellt. Siehe [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Alle Netzen in der Datei werden in einem Ausgabe Mesh reduziert. Wenn die Datei eine Frame Hierarchie enthält, werden alle Transformationen auf das Mesh angewendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Animations Funktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
