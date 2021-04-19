---
description: Die Statistik Struktur enthält Statistiken für die Erfassung. Einige dieser Statistiken werden von Netzwerkmonitor generiert, während andere von der NIC generiert werden, mit der der NPP verbunden ist.
ms.assetid: 5e30ae30-d8ad-4336-9e4d-fa10ceefc966
title: Statistik Struktur (Netmon. h)
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
ms.openlocfilehash: a3798f32f7341722432441272eded7d7605cf8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356652"
---
# <a name="statistics-structure"></a>Statistik Struktur

Die **Statistik** Struktur enthält Statistiken für die Erfassung. Einige dieser Statistiken werden von Netzwerkmonitor generiert, während andere von der NIC generiert werden, mit der der NPP verbunden ist.

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

**Verstrichene Zeit**
</dt> <dd>

Verstrichene Zeit in Mikrosekunden.

</dd> <dt>

**Totalframeseraufgezeichnet**
</dt> <dd>

Gesamtanzahl der aktuell gespeicherten Frames. Diese Anzahl wird durch die Größe der Erfassungs Datei oder des Puffers beschränkt, die zum Speichern der Rahmen verwendet wird.

</dd> <dt>

**Totalbytescaptured**
</dt> <dd>

Gesamtanzahl der aktuell gespeicherten Bytes. Diese Anzahl wird durch die Größe der Erfassungs Datei oder des Puffers beschränkt, die zum Speichern der Rahmen verwendet wird.

</dd> <dt>

**Totalframesgefilterte**
</dt> <dd>

Gesamtanzahl der Frames, die den aktuellen Erfassungs Filter durchlaufen haben. Wenn ein Filter nicht verwendet wird, ist dieser Wert mit **totalframesseen** identisch.

</dd> <dt>

**Totalbytesgefiltert**
</dt> <dd>

Gesamtanzahl der Frames, die den aktuellen Erfassungs Filter durchlaufen haben. Wenn ein Filter nicht verwendet wird, ist dieser Wert mit **totalbytesseen** identisch.

</dd> <dt>

**Totalmulticastsgefilterte**
</dt> <dd>

Dieser Member ist veraltet.

</dd> <dt>

**Totalbroadcastsgefilterte**
</dt> <dd>

Dieser Member ist veraltet.

</dd> <dt>

**Totalframesseen**
</dt> <dd>

Gesamtanzahl der von der NIC behandelten Frames.

</dd> <dt>

**Totalbytesseen**
</dt> <dd>

Gesamtanzahl der Bytes, die von der NIC verarbeitet werden.

</dd> <dt>

**Totalmulticastsempfangene**
</dt> <dd>

Dieser Member ist veraltet.

</dd> <dt>

**Totalbroadcastsempfangene**
</dt> <dd>

Dieser Member ist veraltet.

</dd> <dt>

**Totalframesdrop**
</dt> <dd>

Gesamtzahl der gelöschten Frames (Frames, die den Filter erfolgreich waren, aber nicht gespeichert wurden).

</dd> <dt>

**Totalframesdroppedfrombuffer**
</dt> <dd>

Anzahl der Frames, die aus der Erfassungs Datei oder dem Puffer gelöscht wurden. Wenn der Puffer voll ist, werden ältere Frames entfernt, um Platz für neue zu schaffen.

</dd> <dt>

**Macframesempfangene**
</dt> <dd>

Anzahl der Frames, die von der NIC berichtet wurden.

</dd> <dt>

**Maccrcerrors**
</dt> <dd>

Anzahl von CRC-Fehlern, die von der NIC gemeldet werden.

</dd> <dt>

**Macbytesreceivedex**
</dt> <dd>

Anzahl von Bytes, die von der NIC berichtet wurden.

</dd> <dt>

**Macframesdrop- \_ nobuffers**
</dt> <dd>

Die Anzahl der Frames, die die NIC meldet, weil kein Pufferspeicher Platz vorhanden ist.

</dd> <dt>

**Macmulticastsempfangene**
</dt> <dd>

Anzahl der mit, die der NIC-Bericht empfangen hat.

</dd> <dt>

**Macbroadcastsempfangene**
</dt> <dd>

Anzahl der Übertragungen, die die NIC meldet.

</dd> <dt>

**Macframesdrop \_ hwerror**
</dt> <dd>

Anzahl der Frames, die die NIC aufgrund von Hardwarefehlern gelöscht hat.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird verwendet, um die [*Gesamtstatistik*](t.md)abzurufen und die aktuelle Erfassung anzuhalten oder zu stoppen.

Die Gesamtstatistik kann nicht abgerufen werden, wenn die [iESP](iesp.md) NPP-Schnittstelle verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idelta-DC:: gettotalstatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

["Irren:: gettotalstatistics"](irtc-gettotalstatistics.md)
</dt> <dt>

[IStats:: gettotalstatistics](istats-gettotalstatistics.md)
</dt> <dt>

[Idelta aydc::P ause](idelaydc-pause.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[Iran::P ause](irtc-pause.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[Idelta aydc:: Beendigung](idelaydc-stop.md)
</dt> <dt>

[IESP:: Beendigung](iesp-stop.md)
</dt> <dt>

[Iran:: Beendigung](irtc-stop.md)
</dt> <dt>

[Istatusc:: Beendigung](istats-stop.md)
</dt> </dl>

 

 




