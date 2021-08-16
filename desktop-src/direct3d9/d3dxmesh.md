---
description: 'D3DXMESH-Enumeration: Flags, die zum Angeben von Erstellungsoptionen für ein Gitternetz verwendet werden.'
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: D3DXMESH-Enumeration (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6b83389ae4d92027245877e24e01621f0d93f123dee9ff4f040586b3e7c5111d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525271"
---
# <a name="d3dxmesh-enumeration"></a>D3DXMESH-Enumeration

Flags, die zum Angeben von Erstellungsoptionen für ein Gitternetz verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32 BIT**
</dt> <dd>

Das Gitternetz verfügt über 32-Bit-Indizes anstelle von 16-Bit-Indizes. Siehe Hinweise.

</dd> <dt>

<span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ DONOTCLIP-Verwendungsflag**](d3dusage.md) für Scheitelpunkt- und Indexpuffer.

</dd> <dt>

<span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH-PUNKTE \_**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ POINTS-Verwendungsflag**](d3dusage.md) für Scheitelpunkt- und Indexpuffer.

</dd> <dt>

<span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ RTPATCHES-Verwendungsflag**](d3dusage.md) für Scheitelpunkt- und Indexpuffer.

</dd> <dt>

<span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**
</dt> <dd>

Wenn Sie dieses Flag angeben, werden der Scheitelpunkt und der Indexpuffer des Gitternetzes mit dem [**\_ NPATCHES-Flag D3DUSAGE**](d3dusage.md) erstellt. Dies ist erforderlich, wenn das Meshobjekt mithilfe der N-Patch-Erweiterung mit Direct3D gerendert werden soll.

</dd> <dt>

<span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**
</dt> <dd>

Verwenden Sie das [**D3DPOOL \_ SYSTEMMEM-Verwendungsflag**](./d3dpool.md) für Scheitelpunktpuffer.

</dd> <dt>

<span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ VERWALTET**
</dt> <dd>

Verwenden Sie das [**D3DPOOL \_ MANAGED-Verwendungsflag**](./d3dpool.md) für Scheitelpunktpuffer.

</dd> <dt>

<span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ WRITEONLY-Verwendungsflag**](d3dusage.md) für Scheitelpunktpuffer.

</dd> <dt>

<span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ DYNAMIC**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ DYNAMIC-Verwendungsflag**](d3dusage.md) für Scheitelpunktpuffer.

</dd> <dt>

<span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ SOFTWAREPROCESSING-Verwendungsflag**](d3dusage.md) für Scheitelpunktpuffer.

</dd> <dt>

<span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**
</dt> <dd>

Verwenden Sie das [**D3DPOOL \_ SYSTEMMEM-Verwendungsflag**](./d3dpool.md) für Indexpuffer.

</dd> <dt>

<span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ VERWALTET**
</dt> <dd>

Verwenden Sie das [**D3DPOOL \_ MANAGED-Verwendungsflag**](./d3dpool.md) für Indexpuffer.

</dd> <dt>

<span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ WRITEONLY-Verwendungsflag**](d3dusage.md) für Indexpuffer.

</dd> <dt>

<span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ DYNAMIC**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ DYNAMIC-Verwendungsflag**](d3dusage.md) für Indexpuffer.

</dd> <dt>

<span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ SOFTWAREPROCESSING-Verwendungsflag**](d3dusage.md) für Indexpuffer.

</dd> <dt>

<span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH \_ VB \_ SHARE**
</dt> <dd>

Erzwingt, dass die geklonten Gitternetze Scheitelpunktpuffer gemeinsam nutzen.

</dd> <dt>

<span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**
</dt> <dd>

Verwenden Sie nur die Hardwareverarbeitung. Bei Geräten im gemischten Modus bewirkt dieses Flag, dass das System Hardware verwendet (sofern in der Hardware unterstützt) oder die Softwareverarbeitung standardmäßig verwendet.

</dd> <dt>

<span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**
</dt> <dd>

Entspricht der Angabe von D3DXMESH \_ VB \_ SYSTEMMEM und D3DXMESH \_ IB \_ SYSTEMMEM.

</dd> <dt>

<span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ VERWALTET**
</dt> <dd>

Entspricht der Angabe von D3DXMESH \_ VB \_ MANAGED und D3DXMESH \_ IB \_ MANAGED.

</dd> <dt>

<span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**
</dt> <dd>

Entspricht der Angabe von D3DXMESH \_ VB \_ WRITEONLY und D3DXMESH \_ IB \_ WRITEONLY.

</dd> <dt>

<span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ DYNAMIC**
</dt> <dd>

Entspricht der Angabe von D3DXMESH \_ VB \_ DYNAMIC und D3DXMESH \_ IB \_ DYNAMIC.

</dd> <dt>

<span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**
</dt> <dd>

Entspricht der Angabe von D3DXMESH \_ VB \_ SOFTWAREPROCESSING und D3DXMESH \_ IB \_ SOFTWAREPROCESSING.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein 32-Bit-Gitternetz (D3DXMESH \_ 32BIT) kann theoretisch (2^32)-1 Gesichter und Scheitelpunkte unterstützen. Die Zuweisung von Arbeitsspeicher für ein Gitternetz, das unter einem 32-Bit-Betriebssystem groß ist, ist jedoch nicht praktikabel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
