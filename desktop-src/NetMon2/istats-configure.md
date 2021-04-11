---
description: Die Configure-Methode übermittelt Informationen zur Aufzeichnungs Konfiguration.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: 'IStats:: Configure-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9f2dddea3132ce81a57f16737c0f90c6277d4efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217799"
---
# <a name="istatsconfigure-method"></a>IStats:: Configure-Methode

Die **configure** -Methode übermittelt Informationen zur Aufzeichnungs Konfiguration.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hconfigurationblob* \[ in\]
</dt> <dd>

Handle für das BLOB, das vom Aufrufer konfiguriert wird.

</dd> <dt>

*herrorblob* \[ vorgenommen\]
</dt> <dd>

Handle für ein fehlerblob, das zusätzliche Fehlerinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ BLOB- \_ Zeichenfolge \_ ungültig**</dt> </dl>         | Die Zeichenfolge wird nicht mit Null beendet.<br/>                                                                                                                                                                                            |
| <dl> <dt>**nmerr- \_ BLOB wurde \_ nicht \_ initialisiert.**</dt> </dl>        | Die Methode " **kreateblob** " wurde nicht aufgerufen.<br/>                                                                                                                                                                                |
| <dl> <dt>**Ungültiges nmerr- \_ \_ BLOB**</dt> </dl>                 | Das Objekt, auf das verwiesen wird, ist kein BLOB.<br/>                                                                                                                                                                                  |
| <dl> <dt>**nmerr- \_ Uplevel- \_ BLOB**</dt> </dl>                 | Die BLOB-Versionsnummer ist falsch.<br/>                                                                                                                                                                                         |
| <dl> <dt>**der nmerr- \_ \_ blobeintrag ist \_ bereits \_ vorhanden.**</dt> </dl>  | Ein BLOB-Eintrag ist bereits vorhanden.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**der nmerr- \_ \_ blobeintrag \_ ist \_ nicht \_ vorhanden.**</dt> </dl> | Für das vom *hconfigurationblob* -Parameter angegebene konfigurationsblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Sehen Sie sich den vom " *herrorblob* "-Parameter zurückgegebenen fehlerblob an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br/> |
| <dl> <dt>**mehrdeutiger nmerr- \_ \_ Spezifizierer**</dt> </dl>          | Im BLOB fehlen Besitzer-oder Kategorieinformationen.<br/>                                                                                                                                                                                 |
| <dl> <dt>**nmerr- \_ BLOB- \_ Besitzer \_ nicht \_ gefunden**</dt> </dl>       | Der Besitzer Abschnitt des BLOBs wurde nicht gefunden.<br/>                                                                                                                                                                                  |
| <dl> <dt>**nmerr- \_ BLOB- \_ Kategorie \_ nicht \_ gefunden**</dt> </dl>    | Der Kategorieabschnitt des BLOBs wurde nicht gefunden.<br/>                                                                                                                                                                               |
| <dl> <dt>**Unbekannte nmerr- \_ \_ Kategorie**</dt> </dl>             | Die Kategorieinformationen wurden gefunden, aber nicht verstanden.<br/>                                                                                                                                                                            |
| <dl> <dt>**Unbekanntes nmerr- \_ \_ Tag**</dt> </dl>                  | Taginformationen wurden gefunden, aber nicht verstanden.<br/>                                                                                                                                                                                 |
| <dl> <dt>**nmerr- \_ BLOB- \_ Konvertierungs \_ Fehler**</dt> </dl>       | Das BLOB ist beschädigt.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**nmerr-Fehler (unzulässig) \_ \_**</dt> </dl>              | Der Auslöse Teil des BLOBs ist beschädigt.<br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Sie müssen diese Methode anwenden, um eine NPP, die gestartet, beendet, aber nicht getrennt wurde, neu zu starten.

Der von *herrorblob* zurückgegebene fehlerblob enthält Einträge, die Netzwerkmonitor im Konfigurations-BLOB, das im *hconfigurationblob* -Parameter angegeben ist, nicht verstehen oder finden konnte. Das zurückgegebene fehlerblob enthält Fehlerinformationen, die von der Anwendung für die Problembehandlung verwendet werden können. Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag Netzwerkmonitor der nicht gefunden wurde, im zurückgegebenen fehlerblob enthalten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats:: Connect](istats-connect.md)
</dt> <dt>

[BlobNetzwerkmonitor](network-monitor-blobs.md)
</dt> </dl>

 

 




