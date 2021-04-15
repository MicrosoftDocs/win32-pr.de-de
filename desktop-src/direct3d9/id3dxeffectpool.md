---
description: Anwendungen verwenden die ID3DXEffectPool-Schnittstelle, um Parameter zu identifizieren, die von den einzelnen Effekten gemeinsam genutzt werden. Weitere Informationen finden Sie unter Parameter Freigabe beim Klonen und freigeben (Direct3D 9). Diese Schnittstelle verfügt über keine Methoden.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: ID3DXEffectPool-Schnittstelle (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394070"
---
# <a name="id3dxeffectpool-interface"></a>ID3DXEffectPool-Schnittstelle

Anwendungen verwenden die **ID3DXEffectPool** -Schnittstelle, um Parameter zu identifizieren, die von den einzelnen Effekten gemeinsam genutzt werden. Weitere Informationen finden Sie unter Parameter Freigabe beim [Klonen und freigeben (Direct3D 9)](cloning-and-sharing.md). Diese Schnittstelle verfügt über keine Methoden.

## <a name="members"></a>Member

Die **ID3DXEffectPool** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="remarks"></a>Bemerkungen

Die ID3DXEffectPool-Schnittstelle wird durch Aufrufen von [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md)abgerufen.

Der LPD3DXEFFECTPOOL-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Schnittstellen](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
