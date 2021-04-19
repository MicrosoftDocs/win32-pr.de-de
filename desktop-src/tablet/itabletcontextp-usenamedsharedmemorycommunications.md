---
description: Richtet Shared Memory-Kommunikation für den Tablet-Kontext ein.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: 'Itabletcontextp:: usenamedsharedmemorycommunications-Methode'
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
ms.openlocfilehash: 81e8c653dd12600ae02fe7e6038de6e6a38786e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349313"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a>Itabletcontextp:: usenamedsharedmemorycommunications-Methode

Richtet Shared Memory-Kommunikation für den Tablet-Kontext ein.

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

*PID* \[ in\]
</dt> <dd>

Die Prozess-ID des Clients, der auf den gemeinsamen Speicher zugreift.

</dd> <dt>

*pszcallersid* \[ in\]
</dt> <dd>

Die Sicherheits-ID des Funktions Aufrufers.

</dd> <dt>

*pszcallerintegratysid* \[ in\]
</dt> <dd>

Die Sicherheits-ID, die die Integrität der aufrufenden Funktion überprüfen kann.

</dd> <dt>

*pdweventmoredataid* \[ vorgenommen\]
</dt> <dd>

Eine ganze Zahl, die zum Erstellen des Namens eines Ereignisses verwendet wird. Das Ereignis gibt an, ob weitere Daten vorhanden sind.

</dd> <dt>

*pdweventclientleseryid* \[ vorgenommen\]
</dt> <dd>

Eine ganze Zahl, die zum Erstellen des Namens eines Ereignisses verwendet wird. Das-Ereignis signalisiert, dass der Client für den Empfang von Daten bereit ist. Das Ereignis wird signalisiert, nachdem neue Daten verarbeitet wurden.

</dd> <dt>

*pdwmutexaccessid* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Zugriffs-ID des freigegebenen Speichers.

</dd> <dt>

*pdwfilemappingid* \[ vorgenommen\]
</dt> <dd>

Eine ganze Zahl, die den freigegebenen Arbeitsspeicher identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die **usenamedsharedmemorycommunications** -Methode ist Teil des Tablet PC Shared Memory-Protokolls. Ein Client ohne erhöhte Rechte übergibt eine Sicherheits-ID (SID) und eine Sicherheits-ID (Integritäts Stufe, Il-sid), sodass der Tablet-Dienst Zugriffs Steuerungs Listen (Access Control Lists, ACL) für den Zugriff auf die freigegebenen Speicher Objekte verwenden kann. Wenn der Client über erweiterte Berechtigungen verfügt, sollte er "remoesharedmemorycommunications" verwenden, bei dem es sich um die API handelt, die aufgerufen wird, wenn der Dienst bereits über eine erhöhte Berechtigung verfügt.

Die [**SharedMemory- \_ Header**](sharedmemory-header.md) Struktur speichert den Shared Memory-Header.

Die [**SharedMemory- \_ Header**](sharedmemory-header.md) Struktur wird aus den Daten umgewandelt, auf die von der Datei Zuordnung verwiesen wird. Die Rohdaten des Pakets folgen dem **SharedMemory- \_ Header**. Unformatierte Paketdaten können aus dem freigegebenen Speicher gelesen werden, wenn das Ereignis, auf das von *pdweventclientleseyid* verwiesen wird, ausgelöst wird.

In der folgenden Liste wird die Abfolge von Ereignissen zum Zugreifen auf und Verwenden von frei gegebenem Speicher beschrieben.

1.  Der Client löst das clientready-Ereignis aus.
2.  Der Client wartet auf das MoreData-Ereignis.
3.  Der Client erhält den Mutex.
4.  Der Client liest Paketdaten aus dem Abschnitt des gemeinsam genutzten Speichers, der auf den Header folgt. Seriennummern werden im gemeinsam genutzten Speicher nach den Paketdaten angezeigt.
5.  Der Client verarbeitet Daten abhängig vom Wert von **dwevent**.
6.  Der Client schreibt-1 (0xFFFFFFFF) in **dwevent**.
7.  Der Client gibt den Mutex frei.
8.  Der Client löst das clientready-Ereignis aus.

Die Ereignis Namen werden erstellt, indem die Ausgabe dieser Methode formatiert wird. Die folgenden Definitionen können in Verbindung mit sprintf oder dem entsprechenden verwendet werden, um die Ereignis Namen zu erstellen.


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



In jeder Definition wird der Abschnitt "% d" durch die Prozess-ID ersetzt, und der Abschnitt "% u" wird durch die in " *pdweventmoredataid* " oder " *pdweventclientread yid*" zurückgegebene Ganzzahl ersetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"US-haredmemorycommunications"**](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[**Itabletcontextp**](itabletcontextp.md)
</dt> </dl>

 

 




