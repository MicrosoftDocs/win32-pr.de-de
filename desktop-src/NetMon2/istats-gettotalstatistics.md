---
description: 'IStats::GetTotalStatistics-Methode: Die GetTotalStatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.'
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: IStats::GetTotalStatistics-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7c98d947ad81dd1f2dc3e0dd19de144729ea8a069aefc12a820548aaeac4d15d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742660"
---
# <a name="istatsgettotalstatistics-method"></a>IStats::GetTotalStatistics-Methode

Die **GetTotalStatistics-Methode** ruft die [*Gesamtstatistik*](t.md) für die aktuelle [*Erfassung*](c.md)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpStats* \[ out\]
</dt> <dd>

Zeiger auf eine [STATISTICS-Struktur,](statistics.md)die die Gesamtstatistik für die Erfassung bereitstellt. Der Aufrufer ist dafür verantwortlich, den von der **STATISTICS-Struktur** verwendeten Arbeitsspeicher zuzuordnen und freizugeben.

</dd> <dt>

*fClearAfterReading* \[ In\]
</dt> <dd>

Flag, das verwendet wird, um Netzwerkmonitor zu informieren, wie der interne Speicher der Gesamtstatistik behandelt werden soll. Die Einstellung TRUE weist Netzwerkmonitor an, den internen Speicher der Gesamtstatistik zu löschen, nachdem die aktuellen Informationen abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>   | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie die [IStats::Verbinden-Methode](istats-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ STATS \_ ONLY**</dt> </dl> | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IStats::Verbinden-Methode.](istats-connect.md)<br/>                                |
| <dl> <dt>**NMERR \_ NICHT \_ ERFASSEN**</dt> </dl>   | Das NPP erfasst keine Daten. Rufen Sie die [IStats::Start-Methode](istats-start.md) auf, um mit der Erfassung von Daten zu beginnen.<br/>                         |



 

## <a name="remarks"></a>Hinweise

Diese Methode gibt Daten nur zurück, während eine Erfassung ausgeführt wird, einschließlich während der Erfassung angehalten wird.

Netzwerkmonitor speichert auch [*Konversationsstatistiken,*](c.md)die durch Aufrufen der [IStats::GetConversationStatistics-Methode](istats-getconversationstatistics.md) abgerufen werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Verbinden](istats-connect.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> <dt>

[IStats::Start,](istats-start.md)
</dt> <dt>

[Statistiken](statistics.md)
</dt> </dl>

 

 




