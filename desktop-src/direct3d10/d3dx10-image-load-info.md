---
description: Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden. Der Wert d3dx10 \_ Default für einen dieser Parameter bewirkt, dass D3DX automatisch den Wert aus der Quelldatei verwendet.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: D3DX10_IMAGE_LOAD_INFO-Struktur (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369319"
---
# <a name="d3dx10_image_load_info-structure"></a>D3dx10 \_ Image \_ Load \_ Info-Struktur

Stellen Sie optional Informationen für Textur Lade-APIs bereit, um zu steuern, wie Texturen geladen werden. Der Wert d3dx10 \_ Default für einen dieser Parameter bewirkt, dass D3DX automatisch den Wert aus der Quelldatei verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Width**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Ziel Breite der Textur. Wenn die tatsächliche Breite der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um dieser Ziel Breite gerecht zu werden.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Zielhöhe der Textur. Wenn die tatsächliche Höhe der Textur größer oder kleiner als dieser Wert ist, wird die Textur zentral hoch-oder herunterskaliert, um an diese Zielhöhe angepasst zu werden.

</dd> <dt>

**Tiefe**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Tiefe der Textur. Dies gilt nur für Volumentexturen.

</dd> <dt>

**Firstmiplevel**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die höchste Auflösung der MipMap-Ebene der Textur. Wenn dieser Wert größer als 0 ist, wird firstmiplevel nach dem Laden der Textur der MipMap-Ebene 0 zugeordnet.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die maximale Anzahl von MipMap-Ebenen, die die Textur enthalten wird. Die Verwendung von 0 oder d3dx10 \_ default bewirkt, dass eine vollständige MipMap-Kette erstellt wird.

</dd> <dt>

**Verwendung**
</dt> <dd>

Type: **[ **d3d10 \_ Usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**

</dd> <dd>

Die Art und Weise, in der die Textur Ressource verwendet werden soll. Siehe [**d3d10 \_ Usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Pipeline Stufen, an die die Textur gebunden werden darf. Siehe [**d3d10 \_ Bind- \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Zugriffsberechtigungen der CPU für die Textur Ressource. Siehe [**d3d10 \_ CPU \_ - \_ Zugriffsflag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).

</dd> <dt>

**Fehlflags**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Verschiedene Ressourcen Eigenschaften (siehe [**d3d10 \_ Resource \_ misc- \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Typ: **[ **DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Das Format, in dem sich die Textur befindet, nachdem Sie geladen wurde. Siehe [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

**Filter**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtert die Textur mithilfe des angegebenen Filters (nur beim erneuten Sampling). Siehe [**d3dx10 \_ Filter- \_ Flag**](d3dx10-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtert die Textur-MIP-Ebenen mithilfe des angegebenen Filters (nur beim Erzeugen von Mipmaps). Gültige Werte sind d3dx10 \_ Filter \_ None, d3dx10 \_ Filter \_ Point, d3dx10 \_ Filter \_ linear oder d3dx10 \_ Filter \_ Dreieck. Siehe [**d3dx10 \_ Filter- \_ Flag**](d3dx10-filter-flag.md).

</dd> <dt>

**psrcinfo**
</dt> <dd>

Type: **[ **d3dx10 \_ Image \_ Info**](d3dx10-image-info.md)\***

</dd> <dd>

Informationen zum ursprünglichen Image. Siehe [**d3dx10 \_ Image \_ Info**](d3dx10-image-info.md). Kann mit [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)oder [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)abgerufen werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie die Struktur initialisieren, können Sie ein beliebiges Element auf d3dx10 default festlegen, \_ und D3DX initialisiert es mit einem Standardwert aus der Quell Textur, wenn die Textur geladen wird.

Diese Struktur kann von APIs verwendet werden, die folgende Aktionen ausführen:

-   Erstellen Sie Ressourcen, z. b. [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) und [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).
-   Erstellen Sie Datenprozessoren, z. b. [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) oder [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
