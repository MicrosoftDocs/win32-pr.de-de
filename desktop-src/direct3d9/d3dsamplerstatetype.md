---
description: Samplerzustände definieren Textur-samplingvorgänge wie Textur Adressierung und Textur Filterung.
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: D3DSAMPLERSTATETYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366449"
---
# <a name="d3dsamplerstatetype-enumeration"></a>D3DSAMPLERSTATETYPE-Enumeration

Samplerzustände definieren Textur-samplingvorgänge wie Textur Adressierung und Textur Filterung. In einigen samplerzuständen ist die Vertexverarbeitung und einige Setup Pixel Verarbeitung eingerichtet. Samplerzustände können mithilfe von stateblocks gespeichert und wieder hergestellt werden (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP \_ adressu**
</dt> <dd>

Der Textur Adress Modus für die u-Koordinate. Der Standardwert ist D3DTADDRESS \_ Wrap. Weitere Informationen finden Sie unter [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ adressssv**
</dt> <dd>

Der Textur Adress Modus für die v-Koordinate. Der Standardwert ist D3DTADDRESS \_ Wrap. Weitere Informationen finden Sie unter [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ AddressW**
</dt> <dd>

Der Textur Adress Modus für die w-Koordinate. Der Standardwert ist D3DTADDRESS \_ Wrap. Weitere Informationen finden Sie unter [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

<span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP \_ BorderColor**
</dt> <dd>

Rahmenfarbe oder Typ [**D3DCOLOR**](d3dcolor.md). Die Standardfarbe ist 0x00000000.

</dd> <dt>

<span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP- \_ MagFilter**
</dt> <dd>

Vergrößerungs Filter vom Typ [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). Der Standardwert ist D3DTEXF \_ Point.

</dd> <dt>

<span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ MinFilter**
</dt> <dd>

Minification Filter vom Typ [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). Der Standardwert ist D3DTEXF \_ Point.

</dd> <dt>

<span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ MipFilter**
</dt> <dd>

Der während der Minimierung zu verwendende Mipmap-Filter. Siehe [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md). Der Standardwert ist D3DTEXF \_ None.

</dd> <dt>

<span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ mipmaplodbias**
</dt> <dd>

MipMap-Ebenen-Detail-Bias. Der Standardwert ist 0 (null).

</dd> <dt>

<span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ MaxMipLevel**
</dt> <dd>

Detail Index der größten zu verwendenden Zuordnung. Die Werte liegen im Bereich von 0 bis (n-1), wobei 0 das größte ist. Der Standardwert ist 0 (null).

</dd> <dt>

<span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ MaxAnisotropy**
</dt> <dd>

DWORD Maximum Anisotropy. Werte liegen zwischen 1 und dem Wert, der im **MaxAnisotropy** -Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur angegeben ist. Der Standardwert ist 1.

</dd> <dt>

<span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ srgbtexture**
</dt> <dd>

Gamma Korrekturwert. Der Standardwert ist 0 (null). das bedeutet, dass Gamma 1,0 ist und keine Korrektur erforderlich ist. Andernfalls bedeutet dieser Wert, dass der Sampler Gamma von 2,2 für den Inhalt annehmen und in linear (Gamma 1,0) konvertieren muss, bevor er dem Pixelshader präsentiert wird.

</dd> <dt>

<span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ Elementindex**
</dt> <dd>

Wenn dem Sampler eine multielementtextur zugewiesen wird, gibt dies an, welcher Element Index verwendet werden soll. Der Standardwert ist 0.

</dd> <dt>

<span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ dmapoffset**
</dt> <dd>

Vertexoffset in der vorab komprimierten Verschiebungs Zuordnung. Dies ist eine Konstante, die vom Mosaik Prozess verwendet wird. der Standardwert ist 0.

</dd> <dt>

<span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
