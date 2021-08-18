---
description: Fordert die Freigabe eines Frameobjekts an.
ms.assetid: b2793744-1bba-4a2b-938c-44ed316358fd
title: ID3DXAllocateHierarchy::D estframe-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f9e827a2bc53c5b87478cceadec5f56e5d41c4ecfd76a0dddf1bac0ee964128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987970"
---
# <a name="id3dxallocatehierarchydestroyframe-method"></a>ID3DXAllocateHierarchy::D estframe-Methode

Fordert die Freigabe eines Frameobjekts an.

## <a name="syntax"></a>Syntax


```C++
HRESULT DestroyFrame(
  [in] LPD3DXFRAME pFrameToFree
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFrameToFree* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**

Zeiger auf den Frame, für den die Lokalisierung wieder möglich ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode so, dass D3D \_ OK zurückgegeben wird. Programmieren Sie andernfalls die -Methode so, dass eine entsprechende Fehlermeldung von D3DERR oder D3DXERR zurückgegeben wird, da dadurch auch [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) fehlschlägt und der Fehler zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




