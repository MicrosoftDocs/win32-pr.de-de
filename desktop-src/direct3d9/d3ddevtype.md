---
description: Definiert Gerätetypen.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: D3DDEVTYPE-Enumeration (D3D9Types.h)
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
ms.openlocfilehash: d311706d328a5d05668a4d1dcddb032f17fba0c69e48286f899875a8da6a650e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732990"
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

<span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE \_ HAI**
</dt> <dd>

Hardwarerasterung. Die Schattierung erfolgt mit Software, Hardware oder gemischter Transformation und Beleuchtung.

</dd> <dt>

<span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NULLREF**
</dt> <dd>

Initialisieren Sie Direct3D auf einem Computer, auf dem weder Hardware noch Verweisrasterung verfügbar ist, und aktivieren Sie Ressourcen für die Erstellung von 3D-Inhalten. Siehe Hinweise.

</dd> <dt>

<span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ REF**
</dt> <dd>

Direct3D-Features werden in Software implementiert. Der Referenzraster verwendet jedoch nach Möglichkeit spezielle CPU-Anweisungen.

Das Referenzgerät wird vom Windows SDK 8.0 oder höher installiert und dient nur zur Unterstützung beim Debuggen für die Entwicklung.

</dd> <dt>

<span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**
</dt> <dd>

Ein austauschbares Softwaregerät, das bei [**IDirect3D9::RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice)registriert wurde.

</dd> <dt>

<span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Alle Methoden der [**IDirect3D9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) die einen **D3DDEVTYPE-Gerätetyp** annehmen, schlagen fehl, wenn D3DDEVTYPE \_ NULLREF angegeben ist. Um diese Methoden zu verwenden, ersetzen Sie D3DDEVTYPE \_ REF im Methodenaufruf.

Ein D3DDEVTYPE \_ REF-Gerät sollte im D3DPOOL \_ SCRATCH-Speicher erstellt werden, es sei denn, Scheitelpunkt- und Indexpuffer sind erforderlich. Um Scheitelpunkt- und Indexpuffer zu unterstützen, erstellen Sie das Gerät im D3DPOOL \_ SYSTEMMEM-Speicher.

Wenn D3dref9.dll installiert ist, verwendet Direct3D den Referenzrasterizer, um einen D3DDEVTYPE \_ REF-Gerätetyp zu erstellen, auch wenn D3DDEVTYPE \_ NULLREF angegeben ist. Wenn D3dref9.dll nicht verfügbar ist und D3DDEVTYPE \_ NULLREF angegeben ist, rendert Direct3D weder die Szene noch stellt sie dar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[**\_D3DDEVICE-ERSTELLUNGSPARAMETER \_**](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
