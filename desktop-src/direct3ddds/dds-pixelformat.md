---
title: DDS_PIXELFORMAT-Struktur (Dds.h)
description: Oberflächenpixelformat.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS_PIXELFORMAT Struktur-DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e2c8d4b5e30a3a5a9a039e27f5704019a6300c
ms.sourcegitcommit: 205567a2a76ad672a493a0203ff9d61271d9df98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/18/2021
ms.locfileid: "122358906"
---
# <a name="dds_pixelformat-structure"></a>DDS \_ PIXELFORMAT-Struktur

Oberflächenpixelformat.

## <a name="syntax"></a>Syntax


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a>Member

<dl> <dt>

**dwSize**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Strukturgröße; auf 32 (Bytes) festgelegt.

</dd> <dt>

**dwFlags**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Werte, die angeben, welcher Datentyp sich auf der Oberfläche befindet.



| Flag              | Beschreibung                                                                                                                                                                                                                                | Wert   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| DDPF \_ ALPHAPIXELS | Textur enthält Alphadaten. **dwRGBAlphaBitMask** enthält gültige Daten.                                                                                                                                                                    | 0x1     |
| DDPF \_ ALPHA       | Wird in einigen älteren DDS-Dateien nur für nicht komprimierte Alphakanaldaten verwendet (dwRGBBitCount enthält die Alphakanalbitcount, dwABitMask enthält gültige Daten)                                                                                  | 0x2     |
| DDPF \_ FOURCC      | Textur enthält komprimierte RGB-Daten. **dwFourCC** enthält gültige Daten.                                                                                                                                                                    | 0x4     |
| DDPF \_ RGB         | Die Textur enthält unkomprimierte RGB-Daten. **dwRGBBitCount** und die RGB-Masken (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) enthalten gültige Daten.                                                                                           | 0x40    |
| DDPF \_ YUV         | Wird in einigen älteren DDS-Dateien für unkomprimierte YUV-Daten verwendet (dwRGBBitCount enthält die YUV-Bitanzahl; dwRBitMask enthält die Y-Maske, dwGBitMask enthält die U-Maske, dwBBitMask enthält die V-Maske).                                          | 0x200   |
| \_DDPF-LEUCHTDICHTE   | Wird in einigen älteren DDS-Dateien für unkomprimierte Daten mit einzelner Kanalfarbe verwendet (dwRGBBitCount enthält die Bitanzahl des Leuchtkanals; dwRBitMask enthält die Kanalmaske). Kann mit DDPF \_ ALPHAPIXELS für eine DDS-Datei mit zwei Kanälen kombiniert werden. | 0x20000 |



 

</dd> <dt>

**dwFourCC**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Vierstellige Codes zum Angeben komprimierter oder benutzerdefinierter Formate. Mögliche Werte *sind: DXT1,* *DXT2,* *DXT3,* *DXT4* oder *DXT5.* Ein FourCC von DX10 gibt die Präsense des erweiterten [**DDS \_ HEADER \_ DXT10-Headers**](dds-header-dxt10.md) an, und der dxgiFormat-Member dieser Struktur gibt das true-Format an. Bei Verwendung eines vierstelligen Codes muss dwFlags *DDPF \_ FOURCC* enthalten.

</dd> <dt>

**dwRGBBitCount**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Bits in einem RGB-Format (möglicherweise einschließlich Alpha). Gültig, wenn **dwFlags** *DDPF \_ RGB,* *DDPF \_ LUMINANCE* oder *DDPF \_ YUV* enthält.

</dd> <dt>

**dwRBitMask**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Rote Maske (oder Leuchtdichte oder Y) zum Lesen von Farbdaten. Beispielsweise wäre die rote Maske im Format A8R8G8B8 0x00ff0000.

</dd> <dt>

**dwGBitMask**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Grüne (oder U)-Maske zum Lesen von Farbdaten. Beispielsweise wäre die grüne Maske im Format A8R8G8B8 0x0000ff00.

</dd> <dt>

**dwBBitMask**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Blaue (oder V)-Maske zum Lesen von Farbdaten. Beispielsweise wäre die blaue Maske im Format A8R8G8B8 0x000000ff.

</dd> <dt>

**dwABitMask**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Alphamaske zum Lesen von Alphadaten. dwFlags muss *DDPF \_ ALPHAPIXELS* oder *DDPF \_ ALPHA* enthalten. Beispielsweise wäre die Alphamaske im Format A8R8G8B8 0xff000000.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um DXGI-Formate wie Gleitkommadaten zu speichern, verwenden Sie **dwFlags** von DDPF \_ FOURCC, und legen **Sie dwFourCC** auf "D", "X", "1", "0" fest. Verwenden Sie den [**DDS \_ HEADER \_ DXT10-Erweiterungsheader,**](dds-header-dxt10.md) um das DXGI-Format im **dxgiFormat-Member** zu speichern.

Beachten Sie, dass es nicht standardmäßige Varianten von DDS-Dateien gibt, bei denen **dwFlags** über DDPF \_ FOURCC verfügt und der **dwFourCC-Wert** direkt auf einen D3DFORMAT- oder DXGI \_ FORMAT-Enumerationswert festgelegt ist. Es ist nicht möglich, die D3DFORMAT- und DXGI \_ FORMAT-Werte mit diesem nicht standardmäßigen Schema zu unterscheiden. Daher wird stattdessen der DX10-Erweiterungsheader empfohlen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dds.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Referenz für DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

