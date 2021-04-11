---
description: Gibt Slice-Steuerungsdaten an.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: DXVA_Slice_HEVC_Short-Struktur (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041551"
---
# <a name="dxva_slice_hevc_short-structure"></a>DXVA- \_ Slice- \_ hevc- \_ kurzstruktur

Gibt Slice-Steuerungsdaten an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a>Member

<dl> <dt>

**Bsnalunitdataloation**
</dt> <dd>

Gibt den Speicherort der NAL-Einheit an.

</dd> <dt>

**Slicebytesinbuffer**
</dt> <dd>

Die Anzahl der Bytes im Bitstrom-Datenpuffer, die dieser Slice-Steuerelement Datenstruktur zugeordnet sind.

</dd> <dt>

**wbadslicechopping**
</dt> <dd>

Wenn eine Off-Host-Bitstrom-Verarbeitung verwendet wird, gibt dieser Wert das ungültige Slice-Segment an und enthält einen der folgenden Werte:



| Anforderung | Wert |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wert | BESCHREIBUNG                                                                                                                                                                                                                                             |
| 0     | Alle Bits für den Slice befinden sich innerhalb des entsprechenden Bitstrom-Daten Puffers.                                                                                                                                                                      |
| 1     | Der Bitstrom-Datenpuffer enthält den Anfang des Slice, jedoch nicht den gesamten Slice, da der Puffer voll ist.                                                                                                                                        |
| 2     | Der Bitstrom-Datenpuffer enthält das Ende des Slice. Der Start des Slice ist nicht enthalten, da sich der Start des Slice im vorherigen Bitstrom-Datenpuffer befand.                                                                  |
| 3     | Der Bitstrom-Datenpuffer enthält den Anfang des Slice nicht, da sich der Start des Slice im vorherigen Bitstrom-Datenpuffer befunden hat und das Ende des Slice nicht enthält, da der aktuelle Bitstrom-Datenpuffer ebenfalls voll ist. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

**DXVA \_ Slice \_ hevc \_ Short** enthält Slice-Steuerungsdaten, die vom Host Software Decoder an den Hardwarebeschleuniger übermittelt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Strukturen](media-foundation-structures.md)
</dt> </dl>

 

 




