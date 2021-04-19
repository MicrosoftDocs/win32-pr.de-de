---
title: DDS_HEADER-Struktur (DDS. h)
description: Beschreibt einen DDS-Dateiheader.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS_HEADER Struktur-DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355165"
---
# <a name="dds_header-structure"></a>DDS- \_ Header Struktur

Beschreibt einen DDS-Dateiheader.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**dwSize**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Größe der Struktur. Dieser Member muss auf 124 festgelegt werden.

</dd> <dt>

**dwFlags**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Flags, die angeben, welche Member gültige Daten enthalten.



| Flag              | Beschreibung                                                  | Wert    |
|-------------------|--------------------------------------------------------------|----------|
| ddsd- \_ Caps        | In jeder DDS-Datei erforderlich.                                 | 0x1      |
| ddsd- \_ Höhe      | In jeder DDS-Datei erforderlich.                                 | 0x2      |
| ddsd- \_ Breite       | In jeder DDS-Datei erforderlich.                                 | 0x4      |
| ddsd- \_ Tonhöhe       | Erforderlich, wenn für eine nicht komprimierte Textur eine Tonhöhe bereitgestellt wird. | 0x8      |
| ddsd- \_ Pixel Format | In jeder DDS-Datei erforderlich.                                 | 0x1000   |
| ddsd \_ mipmapcount | Erforderlich in einer Mipmapping-Textur.                             | 0x20000  |
| ddsd \_ linearsize  | Erforderlich, wenn für eine komprimierte Textur eine Tonhöhe bereitgestellt wird.    | 0x80000  |
| ddsd- \_ Tiefe       | In einer tiefen Textur erforderlich.                                 | 0x800000 |



 

> [!Note]  
> Wenn Sie DDS-Dateien schreiben, sollten Sie die ddsd \_ Caps-und ddsd- \_ Pixel Formatflags festlegen. für mipzugeordnete Texturen sollten Sie auch das ddsd- \_ Flag "mipmapcount" festlegen. Wenn Sie jedoch eine DDS-Datei lesen, sollten Sie sich nicht darauf verlassen, dass die \_ Flags ddsd Caps, ddsd \_ Pixel Format und ddsd \_ mipmapcount festgelegt werden, da einige Writer einer solchen Datei diese Flags möglicherweise nicht festlegen.

 

Das \_ \_ \_ in DDS. h definierte DDS-Header Kennzeichen-Textur Kennzeichen ist eine bitweise OR-Kombination aus den ddsd- \_ Caps-, ddsd \_ height-, ddsd \_ Width-und ddsd \_ Pixel Format-Flags.

Das MipMap-Flag für DDS- \_ Header \_ \_ , das in DDS. h definiert ist, entspricht dem ddsd \_ mipmapcount-Flag.

Das \_ \_ \_ in DDS. h definierte DDS-Header Kennzeichen-volumenflag ist gleich dem ddsd- \_ tiefen Flag.

Das \_ \_ \_ in DDS. h definierte DDS-Header Kennzeichen-pitchflag ist gleich dem ddsd- \_ pitchflag.

Das \_ \_ \_ in DDS. h definierte DDS-Header Kennzeichen linearsize-Flag ist gleich dem ddsd \_ linearsize-Flag.

</dd> <dt>

**dwheight**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Oberflächen Höhe (in Pixel).

</dd> <dt>

**dwwidth**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Oberflächen Breite (in Pixel).

</dd> <dt>

**dwpitchorlinearsize**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Größe und die Anzahl der Bytes pro Scan Zeile in einer unkomprimierten Textur. die Gesamtanzahl der Bytes in der Textur der obersten Ebene für eine komprimierte Textur. Weitere Informationen zum Berechnen der Tonhöhe finden Sie im Abschnitt DDS-Datei Layout des [Programmier Handbuchs für DDS](dx-graphics-dds-pguide.md).

</dd> <dt>

**dwtiefe**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Tiefe einer volumetextur (in Pixel), andernfalls nicht verwendet.

</dd> <dt>

**dwmipmapcount**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl von MipMap-Ebenen, andernfalls nicht verwendet.

</dd> <dt>

**dwReserved1 \[ 11\]**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nicht verwendet.

</dd> <dt>

**ddspf**
</dt> <dd>

Typ: **[ **DDS \_ Pixel Format**](dds-pixelformat.md)**

</dd> <dd>

Das Pixel Format (siehe [**DDS \_ Pixel Format**](dds-pixelformat.md)).

</dd> <dt>

**dwcaps**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Gibt die Komplexität der gespeicherten Oberflächen an.



| Flag             | Beschreibung                                                                                                                              | Wert    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| DDSCAPS \_ Komplex | Optionale muss für jede Datei verwendet werden, die mehr als eine Oberfläche (eine MipMap, eine kubische Umgebungs Zuordnung oder eine mipzugeordnete volumetextur) enthält. | 0x8      |
| DDSCAPS- \_ MipMap  | Optionale sollte für eine MipMap verwendet werden.                                                                                                   | 0x400000 |
| DDSCAPS- \_ Textur | Erforderlich                                                                                                                                 | 0x1000   |



 

> [!Note]  
> Wenn Sie DDS-Dateien schreiben, sollten Sie das DDSCAPS \_ -Textur Kennzeichen festlegen, und für mehrere Oberflächen sollten Sie auch das komplexe DDSCAPS- \_ Flag festlegen. Wenn Sie jedoch eine DDS-Datei lesen, sollten Sie sich nicht darauf verlassen, dass die komplexen DDSCAPS \_ -Textur-und DDSCAPS- \_ Flags festgelegt werden, da einige Writer einer solchen Datei diese Flags möglicherweise nicht festlegen.

 

Das in " \_ \_ \_ DDS. h" definierte Flag "Mipmap" der DDS-oberflächenflags ist eine bitweise OR-Kombination aus den komplexen DDSCAPS- \_ und DDSCAPS- \_ MipMap-Flags.

Das Textur Kennzeichen der DDS- \_ Surface- \_ Flags \_ , das in DDS. h definiert ist, entspricht dem DDSCAPS- \_ Textur Kennzeichen.

Das cubemap-Flag der DDS- \_ Surface- \_ Flags \_ , das in DDS. h definiert ist, entspricht dem komplexen DDSCAPS- \_ Flag.

</dd> <dt>

**dwCaps2**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Weitere Details zu den gespeicherten Oberflächen.



| Flag                         | Beschreibung                                            | Wert    |
|------------------------------|--------------------------------------------------------|----------|
| DDSCAPS2 \_ cubemap            | Erforderlich für eine cubemap.                               | 0x200    |
| DDSCAPS2 \_ cubemap \_ positivex | Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden. | 0x400    |
| DDSCAPS2 \_ cubemap \_ negativex | Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden. | 0x800    |
| DDSCAPS2 \_ cubemap \_ positivey | Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden. | 0x1000   |
| DDSCAPS2 \_ cubemap \_ negativey | Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden. | 0x2000   |
| DDSCAPS2 \_ cubemap \_ positivez | Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden. | 0x4000   |
| DDSCAPS2 \_ cubemap \_ negativez | Erforderlich, wenn diese Oberflächen in einer cubemap gespeichert werden. | 0x8000   |
| DDSCAPS2- \_ Volume             | Erforderlich für eine volumetextur.                         | 0x200000 |



 

Das \_ \_ in DDS. h definierte DDS-cubemap positivex-Flag ist eine bitweise OR-Kombination der DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap \_ positivex-Flags.

Das DDS \_ cubemap \_ negativex-Flag, das in DDS. h definiert ist, ist eine bitweise OR-Kombination der DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap \_ negativex-Flags.

Das \_ \_ in DDS. h definierte Flag "DDS cubemap positivey" ist eine bitweise OR-Kombination aus den DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap- \_ Flags.

Das DDS \_ -cubemap \_ -negativey-Flag, das in DDS. h definiert ist, ist eine bitweise OR-Kombination der DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap \_ negativey-Flags.

Das \_ \_ in DDS. h definierte DDS-cubemap-Element, das in DDS. h definiert ist, ist eine bitweise OR-Kombination aus den DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap \_ positivez-Flags.

Das DDS \_ -cubemap \_ negativez-Flag, das in DDS. h definiert ist, ist eine bitweise OR-Kombination der DDSCAPS2 \_ cubemap-und DDSCAPS2 \_ cubemap \_ negativez-Flags.

Das Flag für die DDS- \_ cubemap \_ allgesichter, die in DDS. h definiert ist, ist eine bitweise OR-Kombination der DDS- \_ cubemap \_ positivex, DDS \_ cubemap \_ negativex, DDS \_ cubemap \_ positivvey, DDS \_ cubemap \_ negativey, DDS \_ cubemap \_ positivvez und DDSCAPS2 \_ cubemap \_ negativez Flags.

Das \_ \_ in DDS. h definierte Flag für das DDS-Flags-Volume ist gleich dem DDSCAPS2- \_ volumenflag.

> [!Note]  
> Obwohl Direct3D 9 partielle Cubemaps, Direct3D 10, 10,1 und 11 unterstützt, müssen Sie alle sechs Cube-Map-Gesichter definieren (d. h., Sie müssen DDS \_ cubemap \_ allgesichter festlegen).

 

</dd> <dt>

**dwCaps3**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nicht verwendet.

</dd> <dt>

**dwCaps4**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nicht verwendet.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Einschließen von Flags in **dwFlags** für die Member der Struktur, die gültige Daten enthalten.

Verwenden Sie diese Struktur in Kombination mit einem [**DDS- \_ Header \_ DXT10**](dds-header-dxt10.md) , um ein Ressourcen Array in einer DDS-Datei zu speichern. Weitere Informationen finden Sie unter [Textur Arrays](dx-graphics-dds-pguide.md).

**DDS \_ Der Header** ist mit der DirectDraw DDSURFACEDESC2-Struktur ohne DirectDraw-Abhängigkeiten identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verweis für DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

