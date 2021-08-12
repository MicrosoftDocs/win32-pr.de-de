---
title: _WAVEFORMATEX-Struktur
description: Die \_WAVEFORMATEX-Struktur definiert das Format von Waveform-Audiodaten.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- _WAVEFORMATEX Struktur von Windows Media Geräte-Manager
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
ms.openlocfilehash: e149608d740df6df40b39b64b09ac11837a721b5b4844f1a73eb52e1b5cea479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586745"
---
# <a name="_waveformatex-structure"></a>\_WAVEFORMATEX-Struktur

Die **\_ WAVEFORMATEX-Struktur** definiert das Format von Waveform-Audiodaten.

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

**wFormatTag**
</dt> <dd>

Muss auf ein Format oder Formate festgelegt werden, die vom Gerät unterstützt werden. Beachten Sie, dass frühere Versionen des Windows Media Geräte-Manager WMDM WAVE FORMAT ALL empfohlen werden, um unterstützung für \_ \_ alle Formate \_ anzugeben. Dies wird jedoch nicht mehr empfohlen, da verschiedene Media Player dies auf unterschiedliche Weise interpretieren, und nur wenige Geräte können wirklich jedes Dateiformat wiedererspielen. Es wird jetzt empfohlen, den WMDM \_ ENUM PROP VALID VALUES ANY-Wert der \_ \_ \_ \_ [**WMDM \_ ENUM \_ PROP VALID VALUES \_ \_ \_ FORM-Enumeration**](wmdm-enum-prop-valid-values-form.md) [**\_ \_ \_**](wmdm-prop-values-range.md) zu verwenden oder besser noch einen Bereich von Formaten mit der WMDM PROP VALUES RANGE-Struktur anzugeben.

</dd> <dt>

**nChannels**
</dt> <dd>

Anzahl der Kanäle in den Waveform-Audiodaten. Atururale Daten verwenden einen Kanal, und Stereodaten verwenden zwei Kanäle.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Stichprobenrate in Stichproben pro Sekunde (Hertz), mit der jeder Kanal abgespielt oder aufgezeichnet werden muss. Allgemeine Werte für **nSamplesPerSec** sind 8,0 Kilohertz (kHz), 11,025 kHz, 22,05 kHz und 44,1 kHz.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Erforderliche durchschnittliche Datenübertragungsrate für das Formattag in Bytes pro Sekunde. Wiedergabe- und Aufzeichnungssoftware kann Puffergrößen mithilfe des **nAvgBytesPerSec-Mitglieds** schätzen.

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Blockausrichtung in Bytes. Die Blockausrichtung ist die minimale atomische Dateneinheit für den **wFormatTag-Formattyp.** Wiedergabe- und Aufzeichnungssoftware muss ein Vielfaches von **nBlockAlign-Datenbytes** gleichzeitig verarbeiten. Von einem Gerät geschriebene und gelesene Daten müssen immer am Anfang eines Blocks beginnen. Beispielsweise ist es nicht möglich, die Wiedergabe von PCM-Daten in der Mitte eines Beispiels richtig zu starten (d. h. an einer Grenze, die nicht blockbündig ist).

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bits pro Beispiel für den **Formattyp wFormatTag.**

</dd> <dt>

**cbSize**
</dt> <dd>

Dieser Member wird ignoriert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[**IMDSPStorage::CreateStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[**IMDSPStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[**IWMDMOperation::GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[**IWMDMOperation::SetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





