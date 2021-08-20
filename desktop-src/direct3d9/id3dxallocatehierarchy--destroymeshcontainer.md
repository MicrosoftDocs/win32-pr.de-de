---
description: Fordert die Freigabe eines Meshcontainerobjekts an.
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: ID3DXAllocateHierarchy::D estmultiMeshContainer-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c24b4dee9490c55644ceab4670cda1109dcc4e1cfde65c661bbe9b3fbc64f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094610"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a>ID3DXAllocateHierarchy::D esthydrMeshContainer-Methode

Fordert die Freigabe eines Meshcontainerobjekts an.

## <a name="syntax"></a>Syntax


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMeshContainerToFree* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

Zeiger auf das Gittermodellcontainerobjekt, für das die Zuordnung freigegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode, um D3D \_ OK zurückzugeben. Programmieren Sie andernfalls die -Methode, um eine entsprechende Fehlermeldung von D3DERR oder D3DXERR zurückzugeben, da dies dazu führt, dass [**auch D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) fehlschlägt, und den Fehler zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




