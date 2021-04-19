---
title: _WAVEFORMATEX Struktur
description: Die \_WAVEFORMATEX-Struktur definiert das Format von Waveform-Audiodaten.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- _WAVEFORMATEX Struktur von Windows-Medien Device Manager
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366956"
---
# <a name="_waveformatex-structure"></a>\_WaveFormatEx-Struktur

Die **\_ WaveFormatEx** -Struktur definiert das Format von Waveform-Audiodaten.

## <a name="syntax"></a>Syntax


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a>Member

<dl> <dt>

**wformattag**
</dt> <dd>

Muss auf ein Format oder auf Formate festgelegt werden, die vom Gerät unterstützt werden. Beachten Sie, dass in früheren Versionen des Windows Media-Device Manager die Verwendung von WMDM \_ Wave \_ Format all empfohlen wird \_ , um die Unterstützung für alle Formate anzugeben. Dies wird jedoch nicht mehr empfohlen, da verschiedene Medienspieler dies auf unterschiedliche Weise interpretieren und nur wenige Geräte das Dateiformat wirklich wiedergeben können. Es wird nun empfohlen, die WMDM- \_ \_ Enumerationswerte \_ gültige \_ Werte \_ für einen beliebigen Wert der Enumeration für [**\_ \_ \_ gültige \_ Werte \_ des WMDM**](wmdm-enum-prop-valid-values-form.md) -Enumerationswerts zu verwenden, oder Sie sollten einen Bereich von Formaten mit der [**WMDM- \_ \_ Werte \_ Bereichs**](wmdm-prop-values-range.md) Struktur angeben.

</dd> <dt>

**nchannels**
</dt> <dd>

Anzahl von Kanälen in den Waveform-Audiodaten. Die Monale Daten verwenden einen Kanal, und Stereodaten verwenden zwei Kanäle.

</dd> <dt>

**nsamplespersec**
</dt> <dd>

Die Stichprobenrate in Samplings pro Sekunde (Hertz), bei der jeder Kanal wiedergegeben oder aufgezeichnet werden muss. Allgemeine Werte für **nsamplespersec** sind 8,0 Kilohertz (kHz), 11,025 kHz, 22,05 kHz und 44,1 kHz.

</dd> <dt>

**navgbytespersec**
</dt> <dd>

Erforderliche durchschnittliche Datenübertragungsrate für das Formattag (in Bytes pro Sekunde). Wiedergabe-und Aufzeichnungssoftware kann die Puffergrößen mit dem **navgbytespersec** -Member schätzen.

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Block Ausrichtung (in Bytes). Die Block Ausrichtung ist die minimale unteilbare Einheit von Daten für den Formattyp " **wformattag** ". Wiedergabe-und Aufzeichnungssoftware muss ein Vielfaches von **nBlockAlign** -Bytes an Daten gleichzeitig verarbeiten. Von einem Gerät geschriebene und gelesene Daten müssen immer am Anfang eines-Blocks gestartet werden. Beispielsweise ist es nicht möglich, in der Mitte eines Beispiels (d. h. an einer Grenze, die nicht Block bündig ist) die Wiedergabe von PCM-Daten zu starten.

</dd> <dt>

**wbitspersample**
</dt> <dd>

Bits pro Sample für den Formattyp " **wformattag** ".

</dd> <dt>

**CBSIZE**
</dt> <dd>

Dieser Member wird ignoriert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imdspdevice:: getformatsupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[**Imdspstorage:: anatestorage**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[**Imdspstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[**Iwmdmdevice:: getformatsupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[**Iwmdmoperation:: getobjectattributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[**Iwmdmoperation:: "abtobjectattributes"**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[**Iwmdmstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





