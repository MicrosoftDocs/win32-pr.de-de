---
title: DDS_PIXELFORMAT-Struktur (DDS. h)
description: Das Oberflächen Pixel Format.
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
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354991"
---
# <a name="dds_pixelformat-structure"></a>DDS- \_ Pixel Format-Struktur

Das Oberflächen Pixel Format.

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

Struktur Größe; auf 32 (Bytes) festgelegt.

</dd> <dt>

**dwFlags**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Werte, die angeben, welche Art von Daten auf der-Oberfläche angezeigt wird.



| Flag              | Beschreibung                                                                                                                                                                                                                                | Wert   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| ddpf- \_ alphabepixel | Textur enthält Alpha Daten; **dwrgbalphabitmask** enthält gültige Daten.                                                                                                                                                                    | 0x1     |
| ddpf- \_ Alpha       | Wird in einigen älteren DDS-Dateien für nicht komprimierte Alphakanäle-Daten verwendet (dwrgbbitcount enthält den Alphakanal bitCount; dwabitmask enthält gültige Daten)                                                                                  | 0x2     |
| ddpf \_ FourCC      | Textur enthält komprimierte RGB-Daten. **dwfourcc** enthält gültige Daten.                                                                                                                                                                    | 0x4     |
| ddpf- \_ RGB         | Textur enthält unkomprimierte RGB-Daten. die **dwrgbbitcount** -und RGB-Masken (**dwrbitmask**, **dwgbitmask**, **dwbbitmask**) enthalten gültige Daten.                                                                                           | 0x40    |
| ddpf \_ YUV         | Wird in einigen älteren DDS-Dateien für unkomprimierte YUV-Daten verwendet (dwrgbbitcount enthält die YUV-Bitanzahl; dwrbitmask enthält die Y-Maske, dwgbitmask enthält die U-Maske, dwbbitmask enthält die V-Maske)                                          | 0x200   |
| ddpf- \_ Leuchtkraft   | Wird in einigen älteren DDS-Dateien für unkomprimierte Daten mit einer einzelnen Kanal Farbe verwendet (dwrgbbitcount enthält die Bitzahl des leuchtenden Kanals; dwrbitmask enthält die Kanalmaske). Kann mit ddpf- \_ alphapixeln für eine DDS-Datei mit zwei Kanälen kombiniert werden. | 0x20000 |



 

</dd> <dt>

**dwfourcc**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Vier Zeichen Codes zum Angeben von komprimierten oder benutzerdefinierten Formaten. Folgende Werte sind möglich: *DXT1*, *DXT2*, *DXT3*, *DXT4* oder *DXT5*. Ein FourCC von DX10 gibt die vorangestellt den erweiterten Header des [**DDS- \_ Headers \_ DXT10**](dds-header-dxt10.md) an, und der dxgiformat-Member dieser Struktur gibt das echte Format an. Bei Verwendung eines aus vier Zeichen bestehende Codes müssen dwFlags den *ddpf \_ FourCC* einschließen.

</dd> <dt>

**dwrgbbitcount**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl von Bits in einem RGB-Format (möglicherweise einschließlich Alpha). Gültig, wenn **dwFlags** *ddpf \_ RGB*, *ddpf \_ Leucht* Kraft oder *ddpf \_ YUV* umfasst.

</dd> <dt>

**dwrbitmaske**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Eine rote (oder lumiannce-oder Y-Maske) zum Lesen von Farbdaten. Bei Angabe des A8R8G8B8-Formats würde die rote Maske beispielsweise 0x00ff0000 lauten.

</dd> <dt>

**dwgbitmaske**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Grüne (oder U) Maske zum Lesen von Farbdaten. Wenn beispielsweise das Format A8R8G8B8 angegeben ist, wäre die grüne Maske 0x0000ff00.

</dd> <dt>

**dwbbitmask**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Blaue (oder V-) Maske zum Lesen von Farbdaten. Bei Angabe des A8R8G8B8-Formats würde die blaue Maske beispielsweise 0x000000ff lauten.

</dd> <dt>

**dwabitmask**
</dt> <dd>

Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Alpha Maske zum Lesen von Alpha-Daten. dwFlags muss *ddpf \_ alphapixels* oder *ddpf \_ Alpha* enthalten. Bei Angabe des A8R8G8B8-Formats würde die Alpha Maske beispielsweise 0xFF000000 lauten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie zum Speichern von DXGI-Formaten, wie z. b. Gleit Komma Daten, die **dwFlags** von ddpf \_ FourCC, und legen Sie **dwfourcc** auf 'd ', ' X ', ' 1 ', ' 0 ' fest. Verwenden Sie den [**DDS- \_ Header \_ DXT10**](dds-header-dxt10.md) -Erweiterungs Header, um das DXGI-Format im **dxgiformat** -Member zu speichern.

Beachten Sie, dass es nicht standardmäßige Varianten von DDS-Dateien gibt, bei denen **dwFlags** den ddpf \_ FourCC hat und der **dwfourcc** -Wert direkt auf einen D3DFORMAT-oder DXGI- \_ formatenumerationswert festgelegt ist. Es ist nicht möglich, die D3DFORMAT-oder DXGI- \_ Format Werte mithilfe dieses nicht standardmäßigen Schemas zu unterscheiden, daher wird stattdessen der DX10-Erweiterungs Header empfohlen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verweis für DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

