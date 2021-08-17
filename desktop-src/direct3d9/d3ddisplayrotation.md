---
description: Gibt an, wie der Monitor, der zum Anzeigen einer Vollbildanwendung verwendet wird, gedreht wird.
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: D3DDISPLAYROTATION-Enumeration (D3d9types.h)
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
ms.openlocfilehash: 8defdc206e88750125d88c50e86484428c0dedbd7c18575e26504d7445cd3f64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804936"
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

<span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**D3DDISPLAYROTATION \_ IDENTITY**
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

## <a name="remarks"></a>Hinweise

Diese Enumeration wird in [**IDirect3D9Ex::GetAdapterDisplayModeEx,**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex) [**IDirect3DDevice9Ex::GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)und [**IDirect3DSwapChain9Ex::GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex)verwendet.

Anwendungen können die Überwachungsrotation selbst mithilfe des [D3DPRESENTFLAG \_ NOAUTOROTATE](d3dpresentflag.md)behandeln. In diesem Fall muss die Anwendung wissen, wie der Monitor gedreht wird, damit er sein Rendering entsprechend anpassen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




