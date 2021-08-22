---
description: Übermittelt Konfigurationsdaten für eine Datenerfassung.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: IRTC::Configure-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8f70674d8e570a2640fe301179b21a9f48ec612a17de69e43bdf5c38db4e65af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063910"
---
# <a name="irtcconfigure-method"></a>IRTC::Configure-Methode

Die [**Configure-Methode**](configure.md) übermittelt Konfigurationsdaten für eine Datenerfassung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hConfigurationBlob* \[ In\]
</dt> <dd>

Ein Handle für das BLOB, das vom Aufrufer konfiguriert wird.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Ein Handle für ein Fehlerblob, das zusätzliche Fehlerdaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_NMERR-BLOB \_ NICHT \_ INITIALISIERT**</dt> </dl>        | Die **CreateBlob-Methode** wurde nicht aufgerufen.<br/>                                                                                                                                                 |
| <dl> <dt>**NMERR \_ INVALID \_ BLOB**</dt> </dl>                 | Das Objekt, auf das verwiesen wird, ist kein BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**NMERR \_ UPLEVEL \_ BLOB**</dt> </dl>                 | Die BLOB-Versionsnummer ist falsch.<br/>                                                                                                                                                          |
| <dl> <dt>**NMERR-BLOBEINTRAG \_ \_ BEREITS \_ \_ VORHANDEN**</dt> </dl>  | Doppeltes BLOB.<br/>                                                                                                                                                                                |
| <dl> <dt>**\_NMERR-BLOBEINTRAG \_ IST NICHT \_ \_ \_ VORHANDEN**</dt> </dl> | Dem von *hConfigurationBlob* angegebenen Konfigurationsblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Zeigen Sie den von *hErrorBlob zurückgegebenen FehlerBLOB an,* um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br/> |
| <dl> <dt>**\_NMERR-MEHRDEUTIGER \_ SPEZIFIZIERER**</dt> </dl>          | Die Blobbesitzer- oder Kategoriedaten fehlen.<br/>                                                                                                                                                    |
| <dl> <dt>**NMERR \_ BLOB OWNER NOT FOUND (NMERR-BLOBBESITZER NICHT \_ \_ \_ GEFUNDEN)**</dt> </dl>       | Der Abschnitt BLOB-Besitzer wurde nicht gefunden.<br/>                                                                                                                                                          |
| <dl> <dt>**\_NMERR-BLOBKATEGORIE \_ \_ NICHT \_ GEFUNDEN**</dt> </dl>    | Der Abschnitt BLOB Category wurde nicht gefunden.<br/>                                                                                                                                                       |
| <dl> <dt>**NMERR \_ UNKNOWN \_ CATEGORY**</dt> </dl>             | Der Abschnitt BLOB-Kategorie wurde gefunden, aber nicht verstanden.<br/>                                                                                                                                       |
| <dl> <dt>**NMERR \_ UNKNOWN \_ TAG**</dt> </dl>                  | Der Abschnitt BLOB-Tag wurde gefunden, aber nicht verstanden.<br/>                                                                                                                                            |
| <dl> <dt>**\_ \_ NMERR-BLOBKONVERTIERUNGSFEHLER \_**</dt> </dl>       | Das BLOB ist beschädigt.<br/>                                                                                                                                                                           |
| <dl> <dt>**NMERR– \_ UNZULÄSSIGER \_ TRIGGER**</dt> </dl>              | Der Triggerteil des BLOB ist beschädigt.<br/>                                                                                                                                                    |
| <dl> <dt>**NMERR-BLOBZEICHENFOLGE \_ \_ \_ UNGÜLTIG**</dt> </dl>         | Die Zeichenfolge wird nicht mit NULL beendet.<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Hinweise

Sie müssen diese Methode anwenden, um ein NPP neu zu starten, das gestartet, beendet, aber nicht getrennt wurde.

Das von *hErrorBlob* zurückgegebene FehlerBLOB enthält Einträge, Netzwerkmonitor in dem in *hConfigurationBlob* angegebenen Konfigurationsblob nicht verstanden oder nicht finden konnten. Das zurückgegebene Fehlerblob enthält Fehlerdaten, die die Anwendung für die Problembehandlung verwenden kann. Wenn beispielsweise NMERR BLOB ENTRY DOES NOT EXIST zurückgegeben wird, wird der Eintrag, Netzwerkmonitor nicht finden kann, \_ \_ in das \_ \_ \_ zurückgegebene FehlerBLOB eingeschlossen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Verbinden](irtc-connect.md)
</dt> <dt>

[Netzwerkmonitor BLOBS](network-monitor-blobs.md)
</dt> </dl>

 

 




