---
description: Die Configure-Methode übermittelt Konfigurationsinformationen zur Erfassung.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: IStats::Configure-Methode (Netmon.h)
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
ms.openlocfilehash: 357d0dd9dbb6e0f57a7ecd3dffcec4c0d1e546ce0bc058ce0144796ca8836113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364967"
---
# <a name="istatsconfigure-method"></a>IStats::Configure-Methode

Die **Configure-Methode** übermittelt Konfigurationsinformationen zur Erfassung.

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

Behandeln Sie das BLOB, das der Aufrufer konfiguriert.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Behandeln sie ein Fehler-BLOB, das zusätzliche Fehlerinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ BLOB \_ STRING \_ INVALID**</dt> </dl>         | Die Zeichenfolge ist nicht NULL-terminiert.<br/>                                                                                                                                                                                            |
| <dl> <dt>**\_NMERR-BLOB \_ NICHT \_ INITIALISIERT**</dt> </dl>        | Die **CreateBlob-Methode** wurde nicht aufgerufen.<br/>                                                                                                                                                                                |
| <dl> <dt>**NMERR \_ UNGÜLTIGES \_ BLOB**</dt> </dl>                 | Das Objekt, auf das gezeigt wird, ist kein BLOB.<br/>                                                                                                                                                                                  |
| <dl> <dt>**NMERR \_ \_ UPLEVEL-BLOB**</dt> </dl>                 | Die BLOB-Versionsnummer ist falsch.<br/>                                                                                                                                                                                         |
| <dl> <dt>**\_NMERR-BLOBEINTRAG \_ \_ BEREITS \_ VORHANDEN**</dt> </dl>  | Ein BLOB-Eintrag ist bereits vorhanden.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**\_NMERR-BLOBEINTRAG \_ IST NICHT \_ \_ \_ VORHANDEN**</dt> </dl> | Dem vom Parameter *hConfigurationBlob* angegebenen Konfigurations-BLOB fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Sehen Sie sich den Fehler BLOB an, der vom *hErrorBlob-Parameter* zurückgegeben wurde, um zu bestimmen, welcher Eintrag nicht gefunden wurde.<br/> |
| <dl> <dt>**NMERR \_ AMBIGUOUS \_ SPECIFIER**</dt> </dl>          | Dem BLOB fehlen Besitzer- oder Kategorieinformationen.<br/>                                                                                                                                                                                 |
| <dl> <dt>**\_NMERR-BLOBBESITZER \_ \_ NICHT \_ GEFUNDEN**</dt> </dl>       | Der Abschnitt Besitzer des BLOB wurde nicht gefunden.<br/>                                                                                                                                                                                  |
| <dl> <dt>**\_NMERR-BLOBKATEGORIE \_ \_ NICHT \_ GEFUNDEN**</dt> </dl>    | Der Abschnitt Category des BLOB wurde nicht gefunden.<br/>                                                                                                                                                                               |
| <dl> <dt>**NMERR \_ UNKNOWN \_ CATEGORY**</dt> </dl>             | Kategorieinformationen wurden gefunden, aber nicht verstanden.<br/>                                                                                                                                                                            |
| <dl> <dt>**NMERR \_ UNKNOWN \_ TAG**</dt> </dl>                  | Taginformationen wurden gefunden, aber nicht verstanden.<br/>                                                                                                                                                                                 |
| <dl> <dt>**\_ \_ NMERR-BLOBKONVERTIERUNGSFEHLER \_**</dt> </dl>       | Das BLOB ist beschädigt.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**NMERR \_ ILLEGAL \_ TRIGGER**</dt> </dl>              | Der Triggerteil des BLOB ist beschädigt.<br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a>Hinweise

Sie müssen diese Methode anwenden, um ein NPP neu zu starten, das gestartet, beendet, aber nicht getrennt wurde.

Das von *hErrorBlob* zurückgegebene Fehlerblob enthält Einträge, die Netzwerkmonitor nicht verstehen oder im Konfigurations-BLOB finden konnten, das im Parameter *hConfigurationBlob* angegeben ist. Das zurückgegebene Fehler-BLOB enthält Fehlerinformationen, die die Anwendung für die Problembehandlung verwenden kann. Wenn z. B. NMERR \_ BLOB ENTRY DOES NOT EXIST zurückgegeben \_ \_ \_ \_ wird, ist der Eintrag, den Netzwerkmonitor nicht finden konnte, im zurückgegebenen Fehlerblob enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[ISTATS::Verbinden](istats-connect.md)
</dt> <dt>

[Netzwerkmonitor BLOBS](network-monitor-blobs.md)
</dt> </dl>

 

 




