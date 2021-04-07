---
description: Die getconversation ationstatistics-Methode ruft Sitzungs-und Stations Informationen zur aktuellen Erfassung ab.
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: 'Untc:: getconversation ationstatistics-Methode (Netmon. h)'
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
ms.openlocfilehash: 758488cb3c3f65922bbf6aac4f39774a5430fc92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864071"
---
# <a name="irtcgetconversationstatistics-method"></a>Untc:: getconversation ationstatistics-Methode

Die **getconversation ationstatistics** -Methode ruft [*Sitzungs*](s.md) -und [*Stations Informationen*](s.md) zur aktuellen Erfassung ab.

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

Zeiger auf ein DWORD, das die Anzahl der für die aktuelle Erfassung aufgezeichneten [*Sitzungen*](s.md) enthält.

</dd> <dt>

*lpsessionstats* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [sessionstats](sessionstats.md) -Struktur.

</dd> <dt>

*nstations* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein DWORD, das die Anzahl der [*Stationen*](s.md) enthält, die für die aktuelle Erfassung aufgezeichnet wurden.

</dd> <dt>

*lpstationstats* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [stationstats](stationstats.md) -Struktur.

</dd> <dt>

*f/oder Lese* \[ Vorgänge in\]
</dt> <dd>

Flag, das verwendet wird, um Netzwerkmonitor anzuweisen, den internen Speicher der [sessionstats](sessionstats.md) -und [stationstats](stationstats.md) -Strukturen zu löschen, nachdem die aktuellen Informationen abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                   | Beschreibung                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>          | Der npp ist nicht mit dem Netzwerk verbunden. Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.<br/>                                                                                                      |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl>          | Der NPP erfasst keine Daten. Wenden Sie zum Starten der Erfassung den Befehl " [irren:: Start](irtc-start.md) " an.<br/>                                                                                                                                 |
| <dl> <dt>**nmerr \_ nicht in \_ Echtzeit**</dt> </dl>           | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".<br/>                                                                                                                          |
| <dl> <dt>**nmerr \_ keine \_ Konversations \_ Statistik**</dt> </dl> | Die Konfiguration für diese Verbindung ist so festgelegt, dass keine Konversations Statistiken gespeichert werden. Um Konversations Statistiken zu speichern, legen Sie die Erfassung fest, legen Sie im konfigurationsblob NoConversation ationstats = Yes fest, und starten Sie die Erfassung erneut.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann nur beim Erfassen von Daten aufgerufen werden. Wenn Sie diese Methode beim Anhalten der aktuellen Erfassung aufzurufen, wird die Methode nicht erfolgreich ausgeführt. Um eine Aufzeichnung zu starten, wenden Sie die Methode " [untc:: Start](irtc-start.md) " an.

Um andere Statistik Typen abzurufen, rufen Sie die Methode " [iritc:: gettotalstatistics](irtc-gettotalstatistics.md) " auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

["Iran"](irtc.md)
</dt> <dt>

[Iran:: Connect](irtc-connect.md)
</dt> <dt>

["Irren:: gettotalstatistics"](irtc-gettotalstatistics.md)
</dt> <dt>

["Iran:: Start"](irtc-start.md)
</dt> <dt>

[Sessionstats](sessionstats.md)
</dt> <dt>

[Stationstats](stationstats.md)
</dt> </dl>

 

 




