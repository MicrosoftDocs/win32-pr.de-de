---
title: DDS_HEADER_DXT10-Struktur (DDS. h)
description: DDS-Header Erweiterung zum Verarbeiten von Ressourcen Arrays, DXGI-Pixel Formate, die nicht den Legacy Strukturen des Microsoft DirectDraw-Pixel Formats zugeordnet sind, sowie zusätzliche Metadaten.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS_HEADER_DXT10 Struktur-DDS
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
ms.openlocfilehash: 9a2f5dd4a6948d38b86b49584db81937ce5148b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364350"
---
# <a name="dds_header_dxt10-structure"></a>DDS- \_ Header \_ DXT10 Struktur

DDS-Header Erweiterung zum Verarbeiten von Ressourcen Arrays, DXGI-Pixel Formate, die nicht den Legacy Strukturen des Microsoft DirectDraw-Pixel Formats zugeordnet sind, sowie zusätzliche Metadaten.

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

**dxgiformat**
</dt> <dd>

Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Das Surface-Pixel-Format (siehe [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

</dd> <dt>

**resourcedimension**
</dt> <dd>

Type: **[ **d3d10- \_ Ressourcen \_ Dimension**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Identifiziert den Ressourcentyp. Die folgenden Werte für diesen Member sind eine Teilmenge der Werte in der [**d3d10- \_ Ressourcen \_ Dimension**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) oder der [**D3D11- \_ ressourcendimensionsenumeration \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) :



| type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                            | Wert |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| DDS- \_ Dimension \_ TEXTURE1D (d3d10 \_ Resource \_ Dimension \_ TEXTURE1D) | Die Ressource ist eine [1D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types). Der **dwwidth** -Member des [**DDS- \_ Headers**](dds-header.md) gibt die Größe der Textur an. In der Regel legen Sie den **dwheight** -Member des **DDS- \_ Headers** auf 1 fest. Außerdem müssen Sie das ddsd \_ height-Flag im **dwFlags** -Member des **DDS- \_ Headers** festlegen.                      | 2     |
| DDS- \_ Dimension \_ TEXTURE2D (d3d10 \_ Resource \_ Dimension \_ TEXTURE2D) | Ressource ist eine [2D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) mit einem Bereich, der von den **dwwidth** -und **dwheight** -Membern des [**DDS- \_ Headers**](dds-header.md)angegeben wird. Sie können diesen Typ auch verwenden, um eine cubemaptextur zu identifizieren. Weitere Informationen zum Identifizieren einer cubemaptextur finden Sie unter die Member " **fehlflag** " und " **arraySize** ". | 3     |
| DDS- \_ Dimension \_ TEXTURE3D (d3d10 \_ Resource \_ Dimension \_ TEXTURE3D) | Ressource ist eine [3D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) mit einem Volume, das durch die **dwwidth**-, **dwheight**-und **dwtiefe** -Member des [**DDS- \_ Headers**](dds-header.md)angegeben wird. Sie müssen auch das ddsd- \_ tiefen Flag im **dwFlags** -Member des **DDS- \_ Headers** festlegen.                                                                   | 4     |



 

</dd> <dt>

**fehlflag**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Identifiziert andere, weniger häufig genutzte Optionen für Ressourcen. Der folgende Wert für diesen Member ist eine Teilmenge der Werte im [**d3d10 \_ \_ ressourcenmisc- \_ Flag**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) oder der [**D3D11 \_ Resource \_ misc \_ Flag**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) -Enumeration:



| type                             | BESCHREIBUNG                                                                                                  | Wert |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| DDS- \_ Ressource \_ misc \_ texturecube | Gibt an, dass eine [2D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) eine cubemaptextur ist. | 0x4   |



 

</dd> <dt>

**arraySize**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Anzahl der Elemente im Array.

Bei einer [2D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) , bei der es sich auch um eine cubemaptextur handelt, stellt diese Zahl die Anzahl der Cubes dar. Diese Zahl entspricht der Zahl im **numcubes** -Member des [**d3d10 \_ Texcube- \_ Arrays \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) oder [**D3D11 \_ Texcube- \_ array \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)). In diesem Fall enthält die DDS-Datei **arraySize** \* 6 2D-Texturen. Weitere Informationen zu diesem Fall finden Sie in der Beschreibung zu " **fehlflag** ".

Für eine [3D-Textur](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types)müssen Sie diese Zahl auf 1 festlegen.

</dd> <dt>

**miscFlags2**
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Enthält zusätzliche Metadaten (zuvor war reserviert). Die unteren 3 Bits geben den Alpha Modus der zugeordneten Ressource an. Die oberen 29 Bits sind reserviert und in der Regel 0.



| type                            | BESCHREIBUNG                                                                                                                              | Wert |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| DDS- \_ alpha \_ Modus \_ unbekannt       | Der Alpha Kanal Inhalt ist unbekannt. Dies ist der Wert für Legacy Dateien, bei dem es sich in der Regel um einen "geraden" Alpha handelt.                 | 0x0   |
| DDS- \_ alpha \_ Modus \_ direkt      | Der Inhalt des Alphakanals wird als "gerade Alpha" verwendet.                                                                             | 0x1   |
| DDS- \_ alpha \_ Modus ist \_ vorab multipliziert. | Für alle Alphakanal Inhalte wird ein prämultipliziertes Alpha verwendet. Die einzigen Legacy Dateiformate, die diese Informationen angeben, sind "DX2" und "DX4". | 0x2   |
| DDS- \_ alpha \_ Modus nicht \_ transparent        | Alle Alphakanal Inhalte sind auf vollständig deckend festgelegt.                                                                                    | 0x3   |
| benutzerdefinierter DDS- \_ alpha \_ Modus \_        | Jeder Alphakanal Inhalt wird als 4. Kanal verwendet und ist nicht für die Darstellung von Transparenz (direkt oder vorab multipliziert) vorgesehen.      | 0x4   |



 

> [!Note]  
> Die Legacy Bibliotheken D3DX 10 und [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) können keine geladen werden. DDS-Datei mit **miscFlags2** ungleich 0 (null).

 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Struktur in Verbindung mit einem [**DDS- \_ Header**](dds-header.md) , um ein Ressourcen Array in einer DDS-Datei zu speichern. Weitere Informationen finden Sie unter [Textur Arrays](dx-graphics-dds-pguide.md).

Dieser Header ist vorhanden, wenn der **dwfourcc** -Member der [**DDS- \_ Pixel Format**](dds-pixelformat.md) -Struktur auf ' DX10 ' festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verweis für DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

