---
description: Die Configure-Methode übermittelt Konfigurationsinformationen für eine Erfassung.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: IESP::Configure-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5ae0fba6885db46d987e59517cdc30dab484974869c67c85a257044e5eec58b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365669"
---
# <a name="iespconfigure-method"></a>IESP::Configure-Methode

Die **Configure-Methode** übermittelt Konfigurationsinformationen für eine Erfassung.

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

Handle für das BLOB, das der Aufrufer konfiguriert.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Handle für ein Fehlerblob, das zusätzliche Fehlerinformationen enthält. Informationen zum Inhalt eines Fehlerblobs finden Sie im Abschnitt "Hinweise" in diesem Thema.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>                | Der NPP ist nicht mit dem Netzwerk verbunden.<br/>                                                                                                                                                               |
| <dl> <dt>**NMERR \_ NICHT \_ ESP**</dt> </dl>                      | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IESP::Verbinden-Methode.](iesp-connect.md)<br/>                                                                                                         |
| <dl> <dt>**NMERR-ERFASSUNG \_**</dt> </dl>                     | Der NPP meldet, dass die Erfassungssitzung gestartet wurde.<br/>                                                                                                                                                  |
| <dl> <dt>**NMERR– \_ UNZULÄSSIGER \_ TRIGGER**</dt> </dl>              | Der Triggerteil des Konfigurationsblobs ist beschädigt.<br/>                                                                                                                                              |
| <dl> <dt>**\_NMERR-BLOBEINTRAG \_ IST NICHT \_ \_ \_ VORHANDEN**</dt> </dl> | Dem von *hConfigurationBlob angegebenen Konfigurationsblob* fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Sehen Sie sich den von *hErrorBlob zurückgegebenen FehlerBLOB* an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br/> |
| <dl> <dt>**\_ \_ NMERR-BLOBKONVERTIERUNGSFEHLER \_**</dt> </dl>       | Das BLOB ist beschädigt.<br/>                                                                                                                                                                                   |
| <dl> <dt>**\_NMERR-BLOB \_ NICHT \_ INITIALISIERT**</dt> </dl>        | Die **CreateBlob-Methode** wurde nicht aufgerufen.<br/>                                                                                                                                                         |
| <dl> <dt>**NMERR \_ INVALID \_ BLOB**</dt> </dl>                 | Das Objekt, auf das verwiesen wird, ist kein BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**NMERR-BLOBZEICHENFOLGE \_ \_ \_ UNGÜLTIG**</dt> </dl>         | Die Zeichenfolge wird nicht mit NULL beendet.<br/>                                                                                                                                                                     |
| <dl> <dt>**NMERR \_ UPLEVEL \_ BLOB**</dt> </dl>                 | Die BLOB-Versionsnummer ist falsch.<br/>                                                                                                                                                                  |
| <dl> <dt>**NMERR \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>               | Es war kein Arbeitsspeicher verfügbar. Fahren Sie Fenster herunter, um Ressourcen frei zu machen.<br/>                                                                                                                                       |
| <dl> <dt>**\_NMERR-TIMEOUT**</dt> </dl>                       | Timeout für die Anforderung.<br/>                                                                                                                                                                             |



 

## <a name="remarks"></a>Hinweise

Sie müssen diese Methode anwenden, um ein NPP neu zu starten, das gestartet und beendet, aber nicht getrennt wurde.

Das vom *hErrorBlob-Parameter* zurückgegebene FehlerBLOB enthält Einträge, die Netzwerkmonitor in dem in *hConfigurationBlob* angegebenen KonfigurationsBLOB nicht verstehen oder finden konnten. Das zurückgegebene Fehlerblob enthält Fehlerinformationen, die die Anwendung für die Problembehandlung verwenden kann. Wenn beispielsweise NMERR BLOB ENTRY DOES NOT EXIST zurückgegeben wird, wird der Eintrag, Netzwerkmonitor nicht finden konnte, \_ \_ in das zurückgegebene \_ \_ Fehlerblob \_ eingeschlossen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

 




