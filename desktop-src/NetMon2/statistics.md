---
description: Die STATISTICS-Struktur stellt Statistiken für die Erfassung bereit. Einige dieser Statistiken werden von Netzwerkmonitor generiert, während andere von der NIC generiert werden, mit der das NPP verbunden ist.
ms.assetid: 5e30ae30-d8ad-4336-9e4d-fa10ceefc966
title: STATISTICS-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATISTICS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 273e6ba9e32337cc65b3dce979d2ff407b904595237b60025e42fc58e57d9823
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778280"
---
# <a name="statistics-structure"></a>STATISTICS-Struktur

Die **STATISTICS-Struktur** stellt Statistiken für die Erfassung bereit. Einige dieser Statistiken werden von Netzwerkmonitor generiert, während andere von der NIC generiert werden, mit der das NPP verbunden ist.

## <a name="syntax"></a>Syntax


```C++
typedef struct _STATISTICS {
  __int64 TimeElapsed;
  DWORD   TotalFramesCaptured;
  DWORD   TotalBytesCaptured;
  DWORD   TotalFramesFiltered;
  DWORD   TotalBytesFiltered;
  DWORD   TotalMulticastsFiltered;
  DWORD   TotalBroadcastsFiltered;
  DWORD   TotalFramesSeen;
  DWORD   TotalBytesSeen;
  DWORD   TotalMulticastsReceived;
  DWORD   TotalBroadcastsReceived;
  DWORD   TotalFramesDropped;
  DWORD   TotalFramesDroppedFromBuffer;
  DWORD   MacFramesReceived;
  DWORD   MacCRCErrors;
  __int64 MacBytesReceivedEx;
  DWORD   MacFramesDropped_NoBuffers;
  DWORD   MacMulticastsReceived;
  DWORD   MacBroadcastsReceived;
  DWORD   MacFramesDropped_HwError;
} STATISTICS, *LPSTATISTICS;
```



## <a name="members"></a>Member

<dl> <dt>

**TimeElapsed**
</dt> <dd>

Verstrichene Zeit in Mikrosekunden.

</dd> <dt>

**TotalFramesCaptured**
</dt> <dd>

Gesamtzahl der derzeit gespeicherten Frames. Diese Anzahl wird durch die Größe der Erfassungsdatei oder des Puffers beschränkt, die zum Speichern der Frames verwendet wird.

</dd> <dt>

**TotalBytesCaptured**
</dt> <dd>

Gesamtzahl der derzeit gespeicherten Bytes. Diese Anzahl wird durch die Größe der Erfassungsdatei oder des Puffers beschränkt, die zum Speichern der Frames verwendet wird.

</dd> <dt>

**TotalFramesFiltered**
</dt> <dd>

Gesamtanzahl der Frames, die durch den aktuellen Erfassungsfilter übergeben wurden. Wenn kein Filter verwendet wird, ist dieser Wert identisch mit **TotalFramesSeen.**

</dd> <dt>

**TotalBytesFiltered**
</dt> <dd>

Gesamtanzahl der Frames, die durch den aktuellen Erfassungsfilter übergeben wurden. Wenn kein Filter verwendet wird, ist dieser Wert identisch mit **TotalBytesSeen.**

</dd> <dt>

**TotalMulticastsFiltered**
</dt> <dd>

Dieser Member ist veraltet.

</dd> <dt>

**TotalBroadcastsFiltered**
</dt> <dd>

Dieser Member ist veraltet.

</dd> <dt>

**TotalFramesSeen**
</dt> <dd>

Gesamtanzahl der von der NIC behandelten Frames.

</dd> <dt>

**TotalBytesSeen**
</dt> <dd>

Gesamtanzahl der von der NIC behandelten Bytes.

</dd> <dt>

**TotalMulticastsReceived**
</dt> <dd>

Dieser Member ist veraltet.

</dd> <dt>

**TotalBroadcastsReceived**
</dt> <dd>

Dieser Member ist veraltet.

</dd> <dt>

**TotalFramesDropped**
</dt> <dd>

Gesamtanzahl der gelöschten Frames (Frames, die den Filter bestanden, aber nicht gespeichert wurden).

</dd> <dt>

**TotalFramesDroppedFromBuffer**
</dt> <dd>

Anzahl der Frames, die aus der Erfassungsdatei oder dem Puffer gelöscht wurden. Wenn der Puffer voll ist, werden ältere Frames entfernt, um Platz für neue zu schaffen.

</dd> <dt>

**MacFramesReceived**
</dt> <dd>

Anzahl der Frames, die von der NIC empfangen wurden.

</dd> <dt>

**MacCRCErrors**
</dt> <dd>

Anzahl der von der NIC gemeldeten CRC-Fehler.

</dd> <dt>

**MacBytesReceivedEx**
</dt> <dd>

Anzahl der Bytes, die von der NIC empfangen wurden.

</dd> <dt>

**MacFramesDropped \_ NoBuffers**
</dt> <dd>

Anzahl der Frames, die die NIC meldet, dass sie aufgrund eines fehlenden Pufferspeichers gelöscht wurden.

</dd> <dt>

**MacMulticastsReceived**
</dt> <dd>

Anzahl der Multicasts, die die NIC empfangen hat.

</dd> <dt>

**MacBroadcastsReceived**
</dt> <dd>

Anzahl empfangener Broadcasts der NIC-Berichte.

</dd> <dt>

**MacFramesDropped \_ HwError**
</dt> <dd>

Die Anzahl der Frames, die die NIC meldet, wurde aufgrund von Hardwarefehlern gelöscht.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird verwendet, um [*Gesamtstatistiken*](t.md)abzurufen und die aktuelle Erfassung anzuhalten oder zu beenden.

Gesamtstatistiken können nicht abgerufen werden, wenn die [IESP-NPP-Schnittstelle](iesp.md) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IStats::GetTotalStatistics](istats-gettotalstatistics.md)
</dt> <dt>

[IDelaydC::P ause](idelaydc-pause.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> <dt>

[IStatsC::Stop](istats-stop.md)
</dt> </dl>

 

 




