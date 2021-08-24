---
title: DDS_HEADER -Struktur (Dds.h)
description: Beschreibt einen DDS-Dateiheader.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS_HEADER-Struktur-DDS
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
ms.openlocfilehash: d974c319206d0a0cbe6abda291e9d376bd6478a5b8eb8ba3ef3bb12f182b1288
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746000"
---
# <a name="dds_header-structure"></a>DDS \_ HEADER-Struktur

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

Flags, um anzugeben, welche Member gültige Daten enthalten.



| Flag              | Beschreibung                                                  | Wert    |
|-------------------|--------------------------------------------------------------|----------|
| \_DDSD-OBERGRENZEN        | In jeder DDS-Datei erforderlich.                                 | 0x1      |
| DDSD \_ HEIGHT      | In jeder DDS-Datei erforderlich.                                 | 0x2      |
| \_DDSD-BREITE       | In jeder DDS-Datei erforderlich.                                 | 0x4      |
| DDSD \_ PITCH       | Erforderlich, wenn die Tonhöhe für eine unkomprimierte Textur bereitgestellt wird. | 0x8      |
| DDSD \_ PIXELFORMAT | In jeder DDS-Datei erforderlich.                                 | 0x1000   |
| DDSD \_ MIPMAPCOUNT | Erforderlich in einer Mipmappentextur.                             | 0x20000  |
| DDSD \_ LINEARSIZE  | Erforderlich, wenn die Tonhöhe für eine komprimierte Textur bereitgestellt wird.    | 0x80000  |
| DDSD \_ DEPTH       | Erforderlich in einer Tiefentextur.                                 | 0x800000 |



 

> [!Note]  
> Wenn Sie DDS-Dateien schreiben, sollten Sie die Flags DDSD CAPS und \_ DDSD PIXELFORMAT festlegen. Für mipmapped-Texturen sollten Sie auch das \_ DDSD \_ MIPMAPCOUNT-Flag festlegen. Wenn Sie jedoch eine DDS-Datei lesen, sollten Sie sich nicht darauf verlassen, dass die \_ Flags DDSD CAPS, DDSD PIXELFORMAT und \_ DDSD MIPMAPCOUNT festgelegt werden, da einige Writer einer solchen Datei diese Flags möglicherweise nicht \_ festlegen.

 

Das TEXTURflag DDS HEADER FLAGS, das in Dds.h definiert ist, ist eine \_ \_ \_ bitweise OR-Kombination der Flags DDSD \_ CAPS, DDSD \_ HEIGHT, DDSD WIDTH und \_ DDSD \_ PIXELFORMAT.

Das in Dds.h definierte MIPMAP-Flag DDS HEADER FLAGS entspricht dem \_ \_ \_ DDSD \_ MIPMAPCOUNT-Flag.

Das \_ volume-Flag DDS HEADER FLAGS, das in Dds.h definiert ist, entspricht dem \_ \_ DDSD \_ DEPTH-Flag.

Das IN Dds.h definierte FLAG \_ "DDS HEADER FLAGS PITCH" ist gleich dem \_ \_ DDSD \_ PITCH-Flag.

Das in Dds.h definierte Flag DDS HEADER FLAGS LINEARSIZE entspricht dem \_ \_ \_ DDSD \_ LINEARSIZE-Flag.

</dd> <dt>

**dwHeight**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Oberflächenhöhe (in Pixel).

</dd> <dt>

**dwWidth**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Oberflächenbreite (in Pixel).

</dd> <dt>

**dwPitchOrLinearSize**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Tonhöhe oder Anzahl von Bytes pro Scanzeile in einer unkomprimierten Textur; Die Gesamtanzahl von Bytes in der Textur der obersten Ebene für eine komprimierte Textur. Informationen zum Berechnen der Tonhöhe finden Sie im Abschnitt DDS-Dateilayout des [Programmierhandbuchs für DDS](dx-graphics-dds-pguide.md).

</dd> <dt>

**dwDepth**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tiefe einer Volumetextur (in Pixel), andernfalls nicht verwendet.

</dd> <dt>

**dwMipMapCount**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Mipmapebenen, andernfalls nicht verwendet.

</dd> <dt>

**dwReserved1 \[ 11\]**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nicht verwendet.

</dd> <dt>

**ddspf**
</dt> <dd>

Typ: **[ **DDS \_ PIXELFORMAT**](dds-pixelformat.md)**

</dd> <dd>

Das Pixelformat (siehe [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)).

</dd> <dt>

**dwCaps**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Gibt die Komplexität der gespeicherten Oberflächen an.



| Flag             | Beschreibung                                                                                                                              | Wert    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| DDSCAPS \_ COMPLEX | Optional; muss für jede Datei verwendet werden, die mehr als eine Oberfläche enthält (eine Mipmap, eine kubische Umgebungskarte oder eine Mipmappen-Volumetextur). | 0x8      |
| DDSCAPS \_ MIPMAP  | Optional; sollte für eine Mipmap verwendet werden.                                                                                                   | 0x400000 |
| DDSCAPS-TEXTUR \_ | Erforderlich                                                                                                                                 | 0x1000   |



 

> [!Note]  
> Wenn Sie DDS-Dateien schreiben, sollten Sie das DDSCAPS TEXTURE-Flag festlegen, und für mehrere Oberflächen sollten Sie auch das \_ DDSCAPS \_ COMPLEX-Flag festlegen. Wenn Sie jedoch eine DDS-Datei lesen, sollten Sie sich nicht darauf verlassen, dass die Flags DDSCAPS TEXTURE und DDSCAPS COMPLEX festgelegt werden, da einige Writer einer solchen Datei diese Flags möglicherweise nicht \_ \_ festlegen.

 

Das in \_ Dds.h definierte MIPMAP-Flag DDS SURFACE FLAGS ist eine \_ \_ bitweise OR-Kombination der DDSCAPS COMPLEX- und \_ DDSCAPS \_ MIPMAP-Flags.

Das DDS \_ SURFACE \_ FLAGS TEXTURE-Flag, das in Dds.h definiert ist, entspricht dem \_ DDSCAPS \_ TEXTURE-Flag.

Das \_ CUBEMAP-Flag DDS SURFACE \_ FLAGS, das in \_ Dds.h definiert ist, entspricht dem DDSCAPS \_ COMPLEX-Flag.

</dd> <dt>

**dwCaps2**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Zusätzliche Details zu den gespeicherten Oberflächen.



| Flag                         | Beschreibung                                            | Wert    |
|------------------------------|--------------------------------------------------------|----------|
| DDSCAPS2 \_ CUBEMAP            | Erforderlich für eine Cubezuordnung.                               | 0x200    |
| DDSCAPS2 \_ CUBEMAP \_ POSITIVEX | Erforderlich, wenn diese Oberflächen in einer Cubemap gespeichert werden. | 0x400    |
| DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX | Erforderlich, wenn diese Oberflächen in einer Cubemap gespeichert werden. | 0x800    |
| DDSCAPS2 \_ CUBEMAP \_ POSITIVEY | Erforderlich, wenn diese Oberflächen in einer Cubemap gespeichert werden. | 0x1000   |
| DDSCAPS2 \_ CUBEMAP \_ NEGATIV | Erforderlich, wenn diese Oberflächen in einer Cubemap gespeichert werden. | 0x2000   |
| DDSCAPS2 \_ CUBEMAP \_ POSITIVEZ | Erforderlich, wenn diese Oberflächen in einer Cubemap gespeichert werden. | 0x4000   |
| DDSCAPS2 \_ CUBEMAP \_ NEGATIVEZ | Erforderlich, wenn diese Oberflächen in einer Cubemap gespeichert werden. | 0x8000   |
| DDSCAPS2-VOLUME \_             | Erforderlich für eine Volumetextur.                         | 0x200000 |



 

Das DDS \_ CUBEMAP \_ POSITIVEX-Flag, das in Dds.h definiert ist, ist eine bitweise OR-Kombination der DDSCAPS2 \_ CUBEMAP- und DDSCAPS2 \_ CUBEMAP \_ POSITIVEX-Flags.

Das DDS \_ CUBEMAP \_ NEGATIVEX-Flag, das in Dds.h definiert ist, ist eine bitweise OR-Kombination der DDSCAPS2 \_ CUBEMAP- und DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX-Flags.

Das DDS \_ CUBEMAP \_ POSITIVEY-Flag, das in Dds.h definiert ist, ist eine bitweise OR-Kombination der DDSCAPS2 \_ CUBEMAP- und DDSCAPS2 \_ CUBEMAP \_ POSITIVEY-Flags.

Das DDS \_ CUBEMAP \_ NEGATIVEY-Flag, das in Dds.h definiert ist, ist eine bitweise OR-Kombination der DDSCAPS2 \_ CUBEMAP- und DDSCAPS2 \_ CUBEMAP \_ NEGATIVEY-Flags.

Das DDS \_ CUBEMAP \_ POSITIVEZ-Flag, das in Dds.h definiert ist, ist eine bitweise OR-Kombination der DDSCAPS2 \_ CUBEMAP- und DDSCAPS2 \_ CUBEMAP \_ POSITIVEZ-Flags.

Das DDS \_ CUBEMAP \_ NEGATIVEZ-Flag, das in Dds.h definiert ist, ist eine bitweise OR-Kombination der Flags DDSCAPS2 \_ CUBEMAP und DDSCAPS2 \_ CUBEMAP \_ NEGATIVEZ.

Das in Dds.h definierte DDS \_ CUBEMAP \_ ALLFACES-Flag ist eine bitweise OR-Kombination der Flags DDS \_ CUBEMAP \_ POSITIVEX, DDS \_ CUBEMAP \_ NEGATIVEX, DDS \_ CUBEMAP \_ POSITIVEY, DDS \_ CUBEMAP \_ NEGATIVEY, DDS \_ CUBEMAP \_ POSITIVEZ und DDSCAPS2 \_ CUBEMAP \_ NEGATIVEZ.

Das DDS \_ FLAGS \_ VOLUME-Flag, das in Dds.h definiert ist, entspricht dem DDSCAPS2 \_ VOLUME-Flag.

> [!Note]  
> Obwohl Direct3D 9 partielle Cubezuordnungen unterstützt, erfordern Direct3D 10, 10.1 und 11, dass Sie alle sechs Cubemap-Gesichter definieren (d. h., Sie müssen DDS \_ CUBEMAP \_ ALLFACES festlegen).

 

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

## <a name="remarks"></a>Hinweise

Schließen Sie Flags in **dwFlags für** die Member der -Struktur ein, die gültige Daten enthalten.

Verwenden Sie diese Struktur in Kombination mit [**einem DDS \_ HEADER \_ DXT10,**](dds-header-dxt10.md) um ein Ressourcenarray in einer DDS-Datei zu speichern. Weitere Informationen finden Sie unter [Texturarrays.](dx-graphics-dds-pguide.md)

**DDS \_ HEADER** ist identisch mit der DirectDraw DDSURFACEDESC2-Struktur ohne DirectDraw-Abhängigkeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dds.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Referenz für DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

