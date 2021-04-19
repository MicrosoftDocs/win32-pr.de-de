---
description: Legt die von rechts ausgebene World-View-Transformation für ein Sprite fest. Ein Aufrufe dieser Methode ist vor dem abgleichen oder Sortieren von Sprites erforderlich.
ms.assetid: 83654e9a-8991-49ec-ab28-cf9063126dbe
title: 'ID3DXSprite:: SetWorldViewRH-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewRH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7521f60f819829fc72ba907b57d4e4eb13682a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353739"
---
# <a name="id3dxspritesetworldviewrh-method"></a>ID3DXSprite:: SetWorldViewRH-Methode

Legt die von rechts ausgebene World-View-Transformation für ein Sprite fest. Ein Aufrufe dieser Methode ist vor dem abgleichen oder Sortieren von Sprites erforderlich.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetWorldViewRH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pworld* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf ein [**D3DXMATRIX**](d3dxmatrix.md) -Wert, der eine Welt Transformation enthält. Wenn der Wert **null** ist, wird die Identitätsmatrix für die weltweite Transformation verwendet.

</dd> <dt>

*PView* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf ein [**D3DXMATRIX**](d3dxmatrix.md) -Wert, der eine Ansichts Transformation enthält. Wenn der Wert **null** ist, wird die Identitätsmatrix für die Ansichts Transformation verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall

## <a name="remarks"></a>Bemerkungen

Ein Aufrufen dieser Methode (oder an [**ID3DXSprite:: SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) ist erforderlich, wenn das Sprite mit dem Flag [D3DXSprite \_ \_ Billboard](d3dxsprite.md), D3DXSprite \_ \_ Sort \_ Tiefe \_ frontbackback oder D3DXSprite \_ \_ Sort \_ Tiefe \_ backto Front Flag in [**ID3DXSprite:: begin**](id3dxsprite--begin.md)gerendert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




