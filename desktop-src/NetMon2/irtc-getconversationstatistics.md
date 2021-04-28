---
description: 'IRTC::GetConversationStatistics-Methode: Die GetConversationStatistics-Methode ruft Sitzungs- und Stationsinformationen zur aktuellen Erfassung ab.'
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: IRTC::GetConversationStatistics-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4d2476f4eb33d7e74d0de8363fa88d5e688a2e73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110698"
---
# <a name="irtcgetconversationstatistics-method"></a>IRTC::GetConversationStatistics-Methode

Die **GetConversationStatistics-Methode** ruft [*Sitzungs-*](s.md) und [*Stationsinformationen*](s.md) zur aktuellen Erfassung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nSessions* \[ out\]
</dt> <dd>

Zeiger auf ein DWORD, das die Anzahl der [*sitzungen*](s.md) enthält, die für die aktuelle Erfassung aufgezeichnet wurden.

</dd> <dt>

*lpSessionStats* \[ out\]
</dt> <dd>

Zeiger auf eine [SESSIONSTATS-Struktur.](sessionstats.md)

</dd> <dt>

*nStations* \[ out\]
</dt> <dd>

Zeiger auf ein DWORD, das die Anzahl der für die aktuelle Erfassung [*aufgezeichneten Stationen*](s.md) enthält.

</dd> <dt>

*lpStationStats* \[ out\]
</dt> <dd>

Zeiger auf eine [STATIONSTATS-Struktur.](stationstats.md)

</dd> <dt>

*fClearAfterReading* \[ In\]
</dt> <dd>

Flag, das Netzwerkmonitor anweisen soll, den internen Speicher der [SESSIONSTATS-](sessionstats.md) und [STATIONSTATS-Strukturen](stationstats.md) zu löschen, nachdem die aktuellen Informationen abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                   | Beschreibung                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>          | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IRTC::Connect](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ NICHT \_ ERFASSEN**</dt> </dl>          | Das NPP erfasst keine Daten. Rufen Sie [IRTC::Start](irtc-start.md) auf, um die Erfassung zu starten.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>           | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)<br/>                                                                                                                          |
| <dl> <dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt> </dl> | Die Konfiguration für diese Verbindung ist so festgelegt, dass keine Konversationsstatistiken gespeichert werden. Um Konversationsstatistiken zu speichern, beenden Sie die Erfassung, legen Sie NoConversationStats = YES im Konfigurations-BLOB fest, und starten Sie dann die Erfassung neu.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann nur aufgerufen werden, während Sie Daten erfassen. Wenn Sie diese Methode aufrufen, während die aktuelle Erfassung angehalten wird, ist die Methode nicht erfolgreich. Um eine Erfassung zu starten, rufen Sie die [IRTC::Start-Methode](irtc-start.md) auf.

Um andere Arten von Statistiken abzurufen, rufen Sie die [IRTC::GetTotalStatistics-Methode](irtc-gettotalstatistics.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Connect](irtc-connect.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




