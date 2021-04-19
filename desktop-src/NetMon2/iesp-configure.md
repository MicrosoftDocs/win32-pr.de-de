---
description: Die Configure-Methode übermittelt Konfigurationsinformationen für eine Erfassung.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'IESP:: Configure-Methode (Netmon. h)'
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
ms.openlocfilehash: 53efbe7eb2887165dacc4cb904822de953b84017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353017"
---
# <a name="iespconfigure-method"></a>IESP:: Configure-Methode

Die **configure** -Methode übermittelt Konfigurationsinformationen für eine Erfassung.

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

Handle für ein fehlerblob, das zusätzliche Fehlerinformationen enthält. Informationen zum Inhalt eines Fehler-BLOB finden Sie im Abschnitt "Hinweise" in diesem Thema.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>                | Der npp ist nicht mit dem Netzwerk verbunden.<br/>                                                                                                                                                               |
| <dl> <dt>**nmerr \_ nicht \_ ESP**</dt> </dl>                      | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iESP:: Connect](iesp-connect.md) -Methode.<br/>                                                                                                         |
| <dl> <dt>**nmerr- \_ Erfassung**</dt> </dl>                     | Der NPP meldet, dass die Erfassungs Sitzung gestartet wurde.<br/>                                                                                                                                                  |
| <dl> <dt>**nmerr-Fehler (unzulässig) \_ \_**</dt> </dl>              | Der Auslöse Teil des konfigurationsblobs ist beschädigt.<br/>                                                                                                                                              |
| <dl> <dt>**der nmerr- \_ \_ blobeintrag \_ ist \_ nicht \_ vorhanden.**</dt> </dl> | Für das von *hconfigurationblob* angegebene konfigurationsblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Sehen Sie sich den von *herrorblob* zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br/> |
| <dl> <dt>**nmerr- \_ BLOB- \_ Konvertierungs \_ Fehler**</dt> </dl>       | Das BLOB ist beschädigt.<br/>                                                                                                                                                                                   |
| <dl> <dt>**nmerr- \_ BLOB wurde \_ nicht \_ initialisiert.**</dt> </dl>        | Die Methode " **kreateblob** " wurde nicht aufgerufen.<br/>                                                                                                                                                         |
| <dl> <dt>**Ungültiges nmerr- \_ \_ BLOB**</dt> </dl>                 | Das Objekt, auf das verwiesen wird, ist kein BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**nmerr- \_ BLOB- \_ Zeichenfolge \_ ungültig**</dt> </dl>         | Die Zeichenfolge wird nicht mit Null beendet.<br/>                                                                                                                                                                     |
| <dl> <dt>**nmerr- \_ Uplevel- \_ BLOB**</dt> </dl>                 | Die BLOB-Versionsnummer ist falsch.<br/>                                                                                                                                                                  |
| <dl> <dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt> </dl>               | Es war kein Arbeitsspeicher verfügbar. Fahren Sie Windows herunter, um Ressourcen freizugeben.<br/>                                                                                                                                       |
| <dl> <dt>**nmerr- \_ Timeout**</dt> </dl>                       | Timeout für die Anforderung.<br/>                                                                                                                                                                             |



 

## <a name="remarks"></a>Bemerkungen

Sie müssen diese Methode anwenden, um eine NPP neu zu starten, die gestartet und beendet wurde, jedoch nicht getrennt ist.

Das vom " *herrorblob* "-Parameter zurückgegebene Fehler-BLOB enthält Einträge, die Netzwerkmonitor in dem in *hconfigurationblob* angegebenen Konfigurations-BLOB nicht verstehen oder finden konnten. Das zurückgegebene fehlerblob enthält Fehlerinformationen, die von der Anwendung für die Problembehandlung verwendet werden können. Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag Netzwerkmonitor der nicht gefunden wurde, im zurückgegebenen fehlerblob enthalten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

 




