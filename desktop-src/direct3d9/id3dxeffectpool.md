---
description: Anwendungen verwenden die ID3DXEffectPool-Schnittstelle, um Parameter zu identifizieren, die für alle Auswirkungen freigegeben werden. Siehe Parameterfreigabe unter Klonen und Freigeben (Direct3D 9). Diese Schnittstelle verfügt über keine Methoden.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: ID3DXEffectPool-Schnittstelle (D3DX9Effect.h)
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
ms.openlocfilehash: 42b7669d974fffde76c8c8f1e7beb4f8d78bf58fda3810130b255d4bc5a693df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118680"
---
# <a name="id3dxeffectpool-interface"></a>ID3DXEffectPool-Schnittstelle

Anwendungen verwenden die **ID3DXEffectPool-Schnittstelle,** um Parameter zu identifizieren, die für alle Auswirkungen freigegeben werden. Weitere Informationen finden Sie unter Parameterfreigabe [unter Klonen und Freigeben (Direct3D 9).](cloning-and-sharing.md) Diese Schnittstelle verfügt über keine Methoden.

## <a name="members"></a>Member

Die **ID3DXEffectPool-Schnittstelle** erbt von der [**IUnknown-Schnittstelle,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) verfügt jedoch nicht über zusätzliche Member.

## <a name="remarks"></a>Hinweise

Die ID3DXEffectPool-Schnittstelle wird durch Aufrufen von [**D3DXCreateEffectPool ermittelt.**](d3dxcreateeffectpool.md)

Der LPD3DXEFFECTPOOL-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effektschnittstellen](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
