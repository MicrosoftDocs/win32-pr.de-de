---
description: 'D3DXLoadMeshHierarchyFromXInMemory-Funktion: Lädt die erste Framehierarchie aus einer X-Datei.'
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: D3DXLoadMeshHierarchyFromXInMemory-Funktion (D3dx9anim.h)
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
ms.openlocfilehash: 85929a4cca88d9547ac0f00861f694932c7566cb3b6f5db6d4e6da189842e712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564810"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a>D3DXLoadMeshHierarchyFromXInMemory-Funktion

Lädt die erste Rahmenhierarchie aus einer X-Datei.

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

*pMemory* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen Puffer, der die Gitternetzhierarchie enthält.

</dd> <dt>

*SizeOfMemory* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Größe des pMemory-Puffers in Bytes.

</dd> <dt>

*MeshOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren Flags aus der [**D3DXMESH-Enumeration,**](./d3dxmesh.md) die Erstellungsoptionen für das Gitternetz angeben.

</dd> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das dem Gittermodell zugeordnete Geräteobjekt.

</dd> <dt>

*pAlloc* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Zeiger auf eine [**ID3DXAllocateHierarchy-Schnittstelle.**](id3dxallocatehierarchy.md)

</dd> <dt>

*pUserDataLoader* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Von der Anwendung bereitgestellte Schnittstelle, die das Laden von Benutzerdaten ermöglicht. Siehe [**ID3DXLoadUserData.**](id3dxloaduserdata.md)

</dd> <dt>

*ppFrameHeirarchy* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)\***

Gibt einen Zeiger auf die geladene Rahmenhierarchie zurück. Siehe [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*ppAnimController* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Gibt einen Zeiger auf den Animationscontroller zurück, der der Animation in der X-Datei entspricht. Dies wird mit Standardspuren und Ereignissen erstellt. Siehe [**ID3DXAnimationController.**](id3dxanimationcontroller.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Alle Gitternetze in der Datei werden in ein Ausgabenetz reduziert. Wenn die Datei eine Rahmenhierarchie enthält, werden alle Transformationen auf das Gitternetz angewendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Animationsfunktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
