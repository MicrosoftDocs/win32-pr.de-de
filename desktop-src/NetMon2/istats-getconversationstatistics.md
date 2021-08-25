---
description: Ruft Sitzungs- und Stationsinformationen zur aktuellen Erfassung ab.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: IStats::GetConversationStatistics-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8e76bad23d79e261a27df5b83a94d4e477b21cde5057bb2587ffb49c93382df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890340"
---
# <a name="istatsgetconversationstatistics-method"></a>IStats::GetConversationStatistics-Methode

Die **GetConversationStatistics-Methode** ruft Sitzungs- und Stationsinformationen zur aktuellen Erfassung ab.

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

Ein Zeiger auf ein DWORD, das die Anzahl der [*sitzungen*](s.md) enthält, die für die aktuelle Erfassung aufgezeichnet wurden.

</dd> <dt>

*lpSessionStats* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**SESSIONSTATS-Struktur.**](sessionstats.md)

</dd> <dt>

*nStations* \[ out\]
</dt> <dd>

Ein Zeiger auf ein DWORD, das die Anzahl der für die aktuelle Erfassung [*aufgezeichneten Stationen*](s.md) enthält.

</dd> <dt>

*lpStationStats* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**STATIONSTATS-Struktur.**](stationstats.md)

</dd> <dt>

*fClearAfterReading* \[ In\]
</dt> <dd>

Flag, das verwendet wird, um Netzwerkmonitor anzuweisen, den internen Speicher der [**SESSIONSTATS-**](sessionstats.md) und [**STATIONSTATS-Strukturen**](stationstats.md) zu löschen, nachdem die aktuellen Daten abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                   | Beschreibung                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>          | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [**IStats::Verbinden**](istats-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ NICHT \_ ERFASSEN**</dt> </dl>          | Das NPP erfasst keine Daten. Rufen Sie [**IStats::Start**](istats-start.md) auf, um die Erfassung zu starten.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ NOT \_ STATS \_ ONLY**</dt> </dl>        | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [**IStats::Verbinden-Methode.**](istats-connect.md)<br/>                                                                                                                         |
| <dl> <dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt> </dl> | Die Konfiguration für diese Verbindung ist so festgelegt, dass keine Konversationsstatistiken gespeichert werden. Um Konversationsstatistiken zu speichern, beenden Sie die Erfassung, legen **Sie NoConversationStats = YES** im Konfigurations-BLOB fest, und starten Sie dann die Erfassung neu.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode kann nur aufgerufen werden, während die Datenerfassung ausgeführt wird. Wenn die aktuelle Erfassung angehalten wird, ist ein Aufruf dieser Methode nicht erfolgreich.

Um eine Erfassung zu starten, rufen Sie die [**IStats::Start-Methode**](istats-start.md) auf. Rufen Sie [**IStats::GetTotalStatistics**](istats-gettotalstatistics.md)auf, um andere Arten von Statistiken abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats::GetTotalStatistics**](istats-gettotalstatistics.md)
</dt> <dt>

[**IStats::Start**](istats-start.md)
</dt> <dt>

[**IStats::Verbinden**](istats-connect.md)
</dt> <dt>

[**SESSIONSTATS**](sessionstats.md)
</dt> <dt>

[**STATIONSTATS**](stationstats.md)
</dt> </dl>

 

 




