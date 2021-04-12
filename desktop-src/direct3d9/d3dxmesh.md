---
description: Flags, die zum Angeben der Erstellungs Optionen für ein Mesh verwendet werden.
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: D3DXMESH-Enumeration (D3dx9mesh. h)
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
ms.openlocfilehash: 602eb38f2113b54ee02477faf3bdd15a6a924abc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354186"
---
# <a name="d3dxmesh-enumeration"></a>D3DXMESH-Enumeration

Flags, die zum Angeben der Erstellungs Optionen für ein Mesh verwendet werden.

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

<span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32-Bit**
</dt> <dd>

Das Mesh verfügt über 32-Bit-Indizes anstelle von 16-Bit-Indizes. Siehe Hinweise.

</dd> <dt>

<span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DoNotClip**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ DoNotClip**](d3dusage.md) -nutzungsflag für Scheitelpunkt-und Index Puffer.

</dd> <dt>

<span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH \_ Punkte**
</dt> <dd>

Verwenden Sie das Usage-Flag [**D3DUSAGE \_ Points**](d3dusage.md) für Scheitelpunkt-und Index Puffer.

</dd> <dt>

<span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ rtpatches**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ rtpatches**](d3dusage.md) Usage-Flag für Scheitelpunkt-und Index Puffer.

</dd> <dt>

<span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ npatches**
</dt> <dd>

Die Angabe dieses Flags bewirkt, dass der Scheitelpunkt und der Index Puffer des Mesh mit dem [**D3DUSAGE \_ npatches**](d3dusage.md) -Flag erstellt werden. Dies ist erforderlich, wenn das Mesh-Objekt mit der N-patcherweiterung mithilfe von Direct3D gerendert werden soll.

</dd> <dt>

<span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ vb \_ SystemMem**
</dt> <dd>

Verwenden Sie das [**D3DPOOL \_ SystemMem**](./d3dpool.md) -nutzungsflag für Scheitelpunkt Puffer.

</dd> <dt>

<span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ vb \_ verwaltet**
</dt> <dd>

Verwenden Sie das [**D3DPOOL \_ Managed**](./d3dpool.md) Usage-Flag für Scheitelpunkt Puffer.

</dd> <dt>

<span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ vb \_ schreibgeschützt**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ Write**](d3dusage.md) -use-Flag für Scheitel Punkte.

</dd> <dt>

<span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ vb \_ dynamisch**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ Dynamic**](d3dusage.md) Usage-Flag für Scheitelpunkt Puffer.

</dd> <dt>

<span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ vb- \_ softwareprocessing**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ softwareprocessing**](d3dusage.md) -nutzungsflag für Scheitelpunkt Puffer.

</dd> <dt>

<span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB-System Arbeitsspeicher \_**
</dt> <dd>

Verwenden Sie das [**D3DPOOL \_ SystemMem**](./d3dpool.md) -nutzungsflag für Index Puffer.

</dd> <dt>

<span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ verwaltet**
</dt> <dd>

Verwenden Sie das [**D3DPOOL \_ Managed**](./d3dpool.md) Usage-Flag für Index Puffer.

</dd> <dt>

<span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ schreibgeschützt**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ Write**](d3dusage.md) -use-Flag für Index Puffer.

</dd> <dt>

<span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ dynamisch**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ Dynamic**](d3dusage.md) Usage-Flag für Index Puffer.

</dd> <dt>

<span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB- \_ softwareprocessing**
</dt> <dd>

Verwenden Sie das [**D3DUSAGE \_ softwareprocessing**](d3dusage.md) -nutzungsflag für Index Puffer.

</dd> <dt>

<span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH \_ vb- \_ Freigabe**
</dt> <dd>

Erzwingt, dass die geklonten Netzen Vertex-Puffer freigeben.

</dd> <dt>

<span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ usehweinzierl**
</dt> <dd>

Verwenden Sie nur die Hardware Verarbeitung. Bei Geräten mit gemischtem Modus bewirkt dieses Flag, dass das System Hardware verwendet (wenn es in der Hardware unterstützt wird) oder die Software Verarbeitung standardmäßig verwendet wird.

</dd> <dt>

<span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SystemMem**
</dt> <dd>

Entspricht der Angabe von D3DXMESH \_ vb \_ SystemMem und D3DXMESH \_ IB \_ SystemMem.

</dd> <dt>

<span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ verwaltet**
</dt> <dd>

Entspricht der Angabe von D3DXMESH \_ vb \_ Managed und D3DXMESH \_ IB \_ Managed.

</dd> <dt>

<span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ schreiben**
</dt> <dd>

Entspricht der Angabe von D3DXMESH \_ vb \_ Write-only und D3DXMESH \_ IB \_ Write.

</dd> <dt>

<span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ dynamisch**
</dt> <dd>

Äquivalent zum Angeben von D3DXMESH \_ vb \_ Dynamic und D3DXMESH \_ IB \_ Dynamic.

</dd> <dt>

<span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ softwareprocessing**
</dt> <dd>

Entspricht der Angabe von D3DXMESH \_ vb \_ softwareprocessing und D3DXMESH \_ IB \_ Software processing.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein 32-Bit-Mesh (D3DXMESH \_ 32bit) kann theoretisch (2 ^ 32)-1 Gesichter und Scheitel Punkte unterstützen. Das belegen von Speicher für ein Mesh, das auf einem 32-Bit-Betriebssystem groß ist, ist jedoch nicht praktikabel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
