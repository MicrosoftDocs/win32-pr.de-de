---
description: Diese Schnittstelle wird von der Anwendung implementiert, um Frame-und Mesh-Containerobjekte zuzuordnen oder freizugeben. Methoden für diese werden beim Laden und zerstören von Frame Hierarchien aufgerufen.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: ID3DXAllocateHierarchy-Schnittstelle (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050926"
---
# <a name="id3dxallocatehierarchy-interface"></a>ID3DXAllocateHierarchy-Schnittstelle

Diese Schnittstelle wird von der Anwendung implementiert, um Frame-und Mesh-Containerobjekte zuzuordnen oder freizugeben. Methoden für diese werden beim Laden und zerstören von Frame Hierarchien aufgerufen.

## <a name="members"></a>Member

Die **ID3DXAllocateHierarchy** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXAllocateHierarchy** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXAllocateHierarchy** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CreateFrame**](id3dxallocatehierarchy--createframe.md)                   | Fordert die Zuordnung eines Frame Objekts an.<br/>            |
| [**"Kreatemeschcontainer"**](id3dxallocatehierarchy--createmeshcontainer.md)   | Fordert die Zuordnung eines Mesh-Container Objekts an.<br/>   |
| [**Destroyframe**](id3dxallocatehierarchy--destroyframe.md)                 | Fordert die Aufhebung der Zuordnung eines Frame Objekts an.<br/>          |
| [**Destroymeschcontainer**](id3dxallocatehierarchy--destroymeshcontainer.md) | Fordert die Aufhebung der Zuordnung eines Mesh-Container Objekts an.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der LPD3DXALLOCATEHIERARCHY-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
