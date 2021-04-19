---
description: Definiert Gerätetypen.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: D3DDEVTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361852"
---
# <a name="d3ddevtype-enumeration"></a>D3DDEVTYPE-Enumeration

Definiert Gerätetypen.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE \_ HAL**
</dt> <dd>

Hardware-rasterisierung. Schattierung erfolgt mit Software, Hardware oder gemischter Transformation und Beleuchtung.

</dd> <dt>

<span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NullRef**
</dt> <dd>

Initialisieren Sie Direct3D auf einem Computer, auf dem weder Hardware noch Verweis-rasterisierung verfügbar ist, und aktivieren Sie Ressourcen für die Erstellung von 3D-Inhalten. Siehe Hinweise.

</dd> <dt>

<span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ Ref**
</dt> <dd>

Direct3D-Funktionen sind in Software implementiert. der verweisrasterizer verwendet jedoch bestimmte CPU-Anweisungen, wenn dies möglich ist.

Das Referenzgerät wird vom Windows SDK 8,0 oder höher installiert und ist als Hilfe beim Debuggen nur für die Entwicklung vorgesehen.

</dd> <dt>

<span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**
</dt> <dd>

Ein austauschbares Software Gerät, das bei [**IDirect3D9:: registersoftwaredevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice)registriert wurde.

</dd> <dt>

<span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Alle Methoden der [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) -Schnittstelle, die einen **D3DDEVTYPE** -Gerätetyp annehmen, schlagen fehl, wenn D3DDEVTYPE \_ NullRef angegeben wird. Um diese Methoden zu verwenden, ersetzen Sie D3DDEVTYPE \_ ref im-Methoden aufzurufen.

Ein D3DDEVTYPE \_ ref-Gerät sollte in D3DPOOL \_ Scratch-Speicher erstellt werden, es sei denn, es sind Scheitelpunkt-und Index Puffer erforderlich. Um Vertex-und Index Puffer zu unterstützen, erstellen Sie das Gerät im D3DPOOL \_ systemarbeits Speicher.

Wenn D3dref9.dll installiert ist, verwendet Direct3D den verweisrasterizer zum Erstellen eines D3DDEVTYPE \_ ref-Gerätetyps, auch wenn D3DDEVTYPE \_ NullRef angegeben wird. Wenn D3dref9.dll nicht verfügbar ist und D3DDEVTYPE \_ NullRef angegeben ist, wird die Szene weder von Direct3D gerbt noch präsentiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[**IDirect3D9:: checkdevicemultisampletype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[**IDirect3D9:: checkabvicetype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[**IDirect3D9:: kreatedevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**IDirect3D9:: getde vicecaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[**D3DDEVICE- \_ Erstellungs \_ Parameter**](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
