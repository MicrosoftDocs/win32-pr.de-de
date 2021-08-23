---
description: Richtet die Shared Memory-Kommunikation für den Tablet-Kontext ein.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: ITabletContextP::UseNamedSharedMemoryCommunications-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: a8ce5d4dde7f3fd678e4ac748a0f148750344a1e5e8da9f6481ad25eafa016a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712230"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a>ITabletContextP::UseNamedSharedMemoryCommunications-Methode

Richtet die Shared Memory-Kommunikation für den Tablet-Kontext ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pid* \[ In\]
</dt> <dd>

Die Prozess-ID des Clients, der auf freigegebenen Speicher zutritt.

</dd> <dt>

*pszCallerSid* \[ In\]
</dt> <dd>

Die Sicherheits-ID des Funktionsaufrufers.

</dd> <dt>

*pszCallerIntegritySid* \[ In\]
</dt> <dd>

Die Sicherheits-ID, die die Integrität der aufrufenden Funktion überprüfen kann.

</dd> <dt>

*pdwEventMoreDataId* \[ out\]
</dt> <dd>

Eine ganze Zahl, die verwendet wird, um den Namen eines Ereignisses zu erstellen. Das -Ereignis gibt an, ob mehr Daten gespeichert sind.

</dd> <dt>

*pdwEventClientReadyId* \[ out\]
</dt> <dd>

Eine ganze Zahl, die verwendet wird, um den Namen eines Ereignisses zu erstellen. Das Ereignis signalisiert, dass der Client zum Empfangen von Daten bereit ist. Das Ereignis wird nach der Verarbeitung neuer Daten signalisiert.

</dd> <dt>

*pdwMutexAccessId* \[ out\]
</dt> <dd>

Ein Zeiger auf den Zugriffsbezeichner des freigegebenen Speichers.

</dd> <dt>

*pdwFileMappingId* \[ out\]
</dt> <dd>

Eine ganze Zahl, die den freigegebenen Speicher identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die **UseNamedSharedMemoryCommunications-Methode** ist Teil des Shared Memory-Protokolls für Tablet-PCs. Ein Client ohne erhöhte Rechte übergibt eine Sicherheits-ID (SID) und eine Integritätsebenen-Sicherheits-ID (IL-SID), damit der Tablet-Dienst Zugriffssteuerungslisten (Access Control Lists, ACL) verwenden kann, um auf die Shared Memory-Objekte zu zugreifen. Wenn der Client über erhöhte Berechtigungen verfügt, sollte er UseSharedMemoryCommunications verwenden. Dies ist die API, die aufgerufen wird, wenn der Dienst bereits über erhöhte Rechte verfügt.

Die [**SHAREDMEMORY \_ HEADER-Struktur**](sharedmemory-header.md) speichert den Shared Memory-Header.

Die [**SHAREDMEMORY \_ HEADER-Struktur**](sharedmemory-header.md) wird aus den Daten, auf die von der Dateizuordnung verwiesen wird, umstrukturiert. Die Rohdaten des Pakets folgen dem **SHAREDMEMORY-HEADER \_**. Unformatierte Paketdaten können aus dem freigegebenen Speicher gelesen werden, wenn das Ereignis ausgelöst wird, auf das *von pdwEventClientReadyId* verwiesen wird.

In der folgenden Liste wird die Abfolge von Ereignissen für den Zugriff auf und die Verwendung von freigegebenen Speicher beschrieben.

1.  Der Client löst das clientReady-Ereignis aus.
2.  Der Client wartet auf das MoreData-Ereignis.
3.  Der Client übernimmt den Mutex.
4.  Der Client liest Paketdaten aus dem Abschnitt des freigegebenen Speichers, der dem Header folgt. Seriennummern werden im freigegebenen Speicher nach den Paketdaten angezeigt.
5.  Der Client verarbeitet Daten abhängig vom Wert von **dwEvent**.
6.  Der Client schreibt -1 (0xFFFFFFFF) in **dwEvent**.
7.  Der Client gibt den Mutex frei.
8.  Der Client löst das clientReady-Ereignis aus.

Die Ereignisnamen werden erstellt, indem die Ausgabe dieser Methode formatiert wird. Die folgenden Definitionen können in Verbindung mit sprintf oder der entsprechenden Definition verwendet werden, um die Ereignisnamen zu erstellen.


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



In jeder Definition wird der Abschnitt %d durch die Prozess-ID ersetzt, und der Abschnitt %u wird durch die ganze Zahl ersetzt, die in *pdwEventMoreDataId* oder *pdwEventClientReadyId* zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[**ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




