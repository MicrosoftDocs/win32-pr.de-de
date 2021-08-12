---
title: DDS_HEADER_DXT10 -Struktur (Dds.h)
description: DDS-Headererweiterung zur Handhabung von Ressourcenarrays, DXGI-Pixelformaten, die nicht den älteren Microsoft DirectDraw-Pixelformatstrukturen und zusätzlichen Metadaten zuordnen.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS_HEADER_DXT10-Struktur-DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da95b65739922861002ab134d33f276adabd19c29d14fdea6432616b6c5edc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289787"
---
# <a name="dds_header_dxt10-structure"></a>DDS \_ HEADER \_ DXT10-Struktur

DDS-Headererweiterung zur Handhabung von Ressourcenarrays, DXGI-Pixelformaten, die nicht den älteren Microsoft DirectDraw-Pixelformatstrukturen und zusätzlichen Metadaten zuordnen.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a>Member

<dl> <dt>

**dxgiFormat**
</dt> <dd>

Typ: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Das Oberflächenpixelformat (siehe [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

</dd> <dt>

**resourceDimension**
</dt> <dd>

Typ: **[ **D3D10 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Identifiziert den Typ der Ressource. Die folgenden Werte für diesen Member sind eine Teilmenge der Werte in der [**Enumeration D3D10 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) oder [**D3D11 \_ RESOURCE \_ DIMENSION:**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension)



| type                                                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                            | Wert |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| DDS \_ DIMENSION \_ TEXTURE1D (D3D10 \_ RESOURCE \_ DIMENSION \_ TEXTURE1D) | Die Ressource ist eine [1D-Textur.](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) Der **dwWidth-Member** von [**DDS \_ HEADER**](dds-header.md) gibt die Größe der Textur an. In der Regel legen Sie den **dwHeight-Member** von **DDS \_ HEADER** auf 1 fest. Sie müssen auch das DDSD \_ HEIGHT-Flag im **dwFlags-Member** von **DDS HEADER \_ festlegen.**                      | 2     |
| DDS \_ DIMENSION \_ TEXTURE2D (D3D10 \_ RESOURCE \_ DIMENSION \_ TEXTURE2D) | Die Ressource ist eine [2D-Textur mit](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) einem Bereich, der durch die **DwWidth-** und **dwHeight-Member** von [**DDS \_ HEADER angegeben wird.**](dds-header.md) Sie können diesen Typ auch verwenden, um eine Cubemaptextur zu identifizieren. Weitere Informationen zum Identifizieren einer Cubemaptextur finden Sie unter miscFlag and arraySize members **(Fehlflag** und **arraySize-Member).** | 3     |
| DDS \_ DIMENSION \_ TEXTURE3D (D3D10 \_ RESOURCE \_ DIMENSION \_ TEXTURE3D) | Die Ressource ist eine [3D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) mit einem Volume, das von **den DwWidth-,** **dwHeight-** und **dwDepth-Membern** von [**DDS \_ HEADER angegeben wird.**](dds-header.md) Sie müssen auch das DDSD \_ DEPTH-Flag im **dwFlags-Member** von **DDS \_ HEADER festlegen.**                                                                   | 4     |



 

</dd> <dt>

**miscFlag**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Identifiziert andere, weniger gängige Optionen für Ressourcen. Der folgende Wert für diesen Member ist eine Teilmenge der Werte in der [**ENUMERATION D3D10 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) oder [**D3D11 \_ RESOURCE \_ MISC \_ FLAG:**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)



| type                             | Beschreibung                                                                                                  | Wert |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| DDS \_ RESOURCE \_ MISC \_ TEXTURECUBE | Gibt an, [dass eine 2D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) eine Cubemaptextur ist. | 0x4   |



 

</dd> <dt>

**arraySize**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Anzahl der Elemente im Array.

Bei einer [2D-Textur,](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) die auch eine Cubemaptextur ist, stellt diese Zahl die Anzahl der Cubes dar. Diese Zahl ist identisch mit der Zahl im **NumCubes-Mitglied** von [**D3D10 \_ TEXCUBE \_ ARRAY \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) oder [**D3D11 \_ TEXCUBE \_ ARRAY \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)). In diesem Fall enthält die DDS-Datei **arraySize** \* 6 2D-Texturen. Weitere Informationen zu diesem Fall finden Sie in der **MiscFlag-Beschreibung.**

Für eine [3D-Textur müssen](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)Sie diese Zahl auf 1 festlegen.

</dd> <dt>

**miscFlags2**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Enthält zusätzliche Metadaten (zuvor reserviert). Die unteren 3 Bits geben den Alphamodus der zugeordneten Ressource an. Die oberen 29 Bits sind reserviert und sind in der Regel 0.



| type                            | Beschreibung                                                                                                                              | Wert |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| DDS \_ ALPHA \_ MODE \_ UNKNOWN       | Der Alphakanalinhalt ist unbekannt. Dies ist der Wert für Legacydateien, der in der Regel als "gerades" Alpha angenommen wird.                 | 0x0   |
| DDS \_ ALPHA \_ MODE \_ STRAIGHT      | Es wird davon ausgegangen, dass für jeden Alphakanalinhalt ein gerades Alpha verwendet wird.                                                                             | 0x1   |
| DDS \_ ALPHA \_ MODE \_ PREMULTIPLIED | Alle Alphakanalinhalte verwenden prämultipliierte Alphas. Die einzigen Legacydateiformate, die diese Informationen angeben, sind "DX2" und "DX4". | 0x2   |
| DDS \_ ALPHA \_ MODE \_ OPAQUE        | Alle Alphakanalinhalte sind vollständig deckend festgelegt.                                                                                    | 0x3   |
| BENUTZERDEFINIERTER \_ \_ DDS-ALPHAMODUS \_        | Alle Alphakanalinhalte werden als 4. Kanal verwendet und dienen nicht zur Darstellung der Transparenz (direkt oder prämultipliiert).      | 0x4   |



 

> [!Note]  
> Die älteren D3DX 10- und [D3DX](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) 11-Hilfsprogrammbibliotheken können keine laden. DDS-Datei **mit miscFlags2** gleich 0 (null).

 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Struktur zusammen mit einem [**\_ DDS-HEADER,**](dds-header.md) um ein Ressourcenarray in einer DDS-Datei zu speichern. Weitere Informationen finden Sie unter [Texturarrays.](dx-graphics-dds-pguide.md)

Dieser Header ist vorhanden, wenn **das dwFourCC-Member** der [**DDS \_ PIXELFORMAT-Struktur**](dds-pixelformat.md) auf "DX10" festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dds.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz für DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

