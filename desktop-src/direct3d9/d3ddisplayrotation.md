---
description: Gibt an, wie der Monitor, der zum Anzeigen einer Vollbildanwendung verwendet wird, gedreht wird.
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: D3DDISPLAYROTATION-Enumeration (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYROTATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 28f4d38dca78f0f34daf931a6bf651b40c1b0a78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363964"
---
# <a name="d3ddisplayrotation-enumeration"></a>D3DDISPLAYROTATION-Enumeration

Gibt an, wie der Monitor, der zum Anzeigen einer Vollbildanwendung verwendet wird, gedreht wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDISPLAYROTATION { 
  D3DDISPLAYROTATION_IDENTITY  = 1,
  D3DDISPLAYROTATION_90        = 2,
  D3DDISPLAYROTATION_180       = 3,
  D3DDISPLAYROTATION_270       = 4
} D3DDISPLAYROTATION;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**D3DDISPLAYROTATION- \_ Identität**
</dt> <dd>

Die Anzeige wird nicht gedreht.

</dd> <dt>

<span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION \_ 90**
</dt> <dd>

Die Anzeige wird um 90 Grad gedreht.

</dd> <dt>

<span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION \_ 180**
</dt> <dd>

Die Anzeige wird um 180 Grad gedreht.

</dd> <dt>

<span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION \_ 270**
</dt> <dd>

Die Anzeige wird um 270 Grad gedreht.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Enumeration wird in " [**IDirect3D9Ex:: getadapterdisplaymodeex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex)", " [**IDirect3DDevice9Ex:: getdisplaymodeex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)" und " [**IDirect3DSwapChain9Ex:: getdisplaymodeex**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex)" verwendet.

Anwendungen können die Monitor Drehung selbst mithilfe von [D3DPRESENTFLAG \_ noautorotate](d3dpresentflag.md)verarbeiten. in diesem Fall muss die Anwendung wissen, wie der Monitor gedreht wird, damit er das Rendering entsprechend anpassen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




