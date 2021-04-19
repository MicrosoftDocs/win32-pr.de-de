---
description: Ruft Sitzungs-und Stations Informationen zur aktuellen Erfassung ab.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'IStats:: getconversation ationstatistics-Methode (Netmon. h)'
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
ms.openlocfilehash: 030fafb4ccf041c2804179f8adf0088ca3fba845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366519"
---
# <a name="istatsgetconversationstatistics-method"></a>IStats:: getconversation ationstatistics-Methode

Die **getconversation ationstatistics** -Methode ruft Sitzungs-und Stations Informationen zur aktuellen Erfassung ab.

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

*nsitzungen* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein DWORD, das die Anzahl der [*Sitzungen*](s.md) enthält, die für die aktuelle Erfassung aufgezeichnet wurden.

</dd> <dt>

*lpsessionstats* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**sessionstats**](sessionstats.md) -Struktur.

</dd> <dt>

*nstations* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein DWORD, das die Anzahl der [*Stationen*](s.md) enthält, die für die aktuelle Erfassung aufgezeichnet wurden.

</dd> <dt>

*lpstationstats* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**stationstats**](stationstats.md) -Struktur.

</dd> <dt>

*f/oder Lese* \[ Vorgänge in\]
</dt> <dd>

Flag, das verwendet wird, um Netzwerkmonitor anzuweisen, den internen Speicher der [**sessionstats**](sessionstats.md) -und [**stationstats**](stationstats.md) -Strukturen nach dem Abrufen der aktuellen Daten zu löschen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                   | Beschreibung                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>          | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie [**iStats:: Connect**](istats-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.<br/>                                                                                                      |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl>          | Der NPP erfasst keine Daten. Nennen Sie [**iStats:: Start**](istats-start.md) , um die Erfassung zu starten.<br/>                                                                                                                                 |
| <dl> <dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt> </dl>        | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [**iStats:: Connect**](istats-connect.md) -Methode.<br/>                                                                                                                         |
| <dl> <dt>**nmerr \_ keine \_ Konversations \_ Statistik**</dt> </dl> | Die Konfiguration für diese Verbindung ist so festgelegt, dass keine Konversations Statistiken gespeichert werden. Wenn Sie die Konversations Statistik speichern möchten, legen Sie die Erfassung fest, legen Sie im konfigurationsblob **NoConversation ationstats = Yes** fest, und starten Sie die Erfassung erneut.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann nur aufgerufen werden, während die Datenerfassung ausgeführt wird. Wenn die aktuelle Erfassung angehalten ist, wird ein-Rückruf dieser Methode nicht erfolgreich ausgeführt.

Um eine Aufzeichnung zu starten, müssen Sie die [**iStats:: Start**](istats-start.md) -Methode abrufen. Um andere Statistik Typen abzurufen, rufen Sie [**iStats:: gettotalstatistics**](istats-gettotalstatistics.md)auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats:: gettotalstatistics**](istats-gettotalstatistics.md)
</dt> <dt>

[**IStats:: Start**](istats-start.md)
</dt> <dt>

[**IStats:: Connect**](istats-connect.md)
</dt> <dt>

[**Sessionstats**](sessionstats.md)
</dt> <dt>

[**Stationstats**](stationstats.md)
</dt> </dl>

 

 




