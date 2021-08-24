---
description: 'IDelaydC::GetConversationStatistics-Methode: Die GetConversationStatistics-Methode ruft Sitzungs- und Stationsinformationen zur aktuellen Erfassung ab.'
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: IDelaydC::GetConversationStatistics-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 60fc768a1b93a752a91d431e79fb3e875416ac2b82b2bad5603e3d4cddaccbaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910570"
---
# <a name="idelaydcgetconversationstatistics-method"></a>IDelaydC::GetConversationStatistics-Methode

Die **GetConversationStatistics-Methode** ruft [*Sitzungs-*](s.md) und [*Stationsinformationen zur*](s.md) aktuellen Erfassung ab.

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

Zeiger auf ein DWORD, das die Anzahl der [*für*](s.md) die aktuelle Erfassung aufgezeichneten Sitzungen enthält.

</dd> <dt>

*lpSessionStats* \[ out\]
</dt> <dd>

Zeiger auf eine [SESSIONSTATS-Struktur.](sessionstats.md)

</dd> <dt>

*nStations* \[ out\]
</dt> <dd>

Zeiger auf ein DWORD, das die Anzahl der für die [*aktuelle*](s.md) Erfassung aufgezeichneten Stationen enthält.

</dd> <dt>

*lpStationStats* \[ out\]
</dt> <dd>

Zeiger auf eine [STATIONSTATS-Struktur.](stationstats.md)

</dd> <dt>

*fClearAfterReading* \[ In\]
</dt> <dd>

Flag, das verwendet wird, Netzwerkmonitor, den internen Speicher der [SESSIONSTATS-](sessionstats.md) und [STATIONSTATS-Strukturen](stationstats.md) zu löschen, nachdem die aktuellen Informationen abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                   | Beschreibung                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>          | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen [Sie IDelaydC::Verbinden,](idelaydc-connect.md) um das NPP mit dem Netzwerk zu verbinden.<br/>                                                                                                  |
| <dl> <dt>**NMERR NOT CAPTURING (NMERR \_ WIRD NICHT \_ ERFASST)**</dt> </dl>          | Der NPP erfasst keine Daten. Rufen [Sie IDelaydC::Start auf,](idelaydc-start.md) um die Erfassung zu starten.<br/>                                                                                                                             |
| <dl> <dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt> </dl>            | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IDelaydC::Verbinden-Methode.](idelaydc-connect.md)<br/>                                                                                                                      |
| <dl> <dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt> </dl> | Die Konfiguration für diese Verbindung ist so festgelegt, dass konversationsstatistiken nicht gespeichert werden. Um Konversationsstatistiken zu speichern, beenden Sie die Erfassung, legen Sie NoConversationStats = YES im Konfigurationsblob fest, und starten Sie die Erfassung neu.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode kann nur während der Datenerfassung aufgerufen werden. Wenn die aktuelle Erfassung angehalten wird, sind Aufrufe dieser Methode nicht erfolgreich. Um eine Erfassung zu starten, rufen Sie die [IDelaydC::Start-Methode](idelaydc-start.md) auf.

Rufen Sie zum Abrufen anderer Statistiktypen [IDelaydC::GetTotalStatistics auf.](idelaydc-gettotalstatistics.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Verbinden](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




