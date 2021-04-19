---
description: Übermittelt Konfigurationsdaten für eine Datenerfassung.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'Untc:: Configure-Methode (Netmon. h)'
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
ms.openlocfilehash: 702a3883acdbb7509d79e76d8fcc73af1e167e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353045"
---
# <a name="irtcconfigure-method"></a>Untc:: Configure-Methode

Die [**configure**](configure.md) -Methode übermittelt Konfigurationsdaten für eine Datenerfassung.

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

Ein Handle für das BLOB, das vom Aufrufer konfiguriert wird.

</dd> <dt>

*herrorblob* \[ vorgenommen\]
</dt> <dd>

Ein Handle für ein fehlerblob, das zusätzliche Fehler Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ BLOB wurde \_ nicht \_ initialisiert.**</dt> </dl>        | Die Methode " **kreateblob** " wurde nicht aufgerufen.<br/>                                                                                                                                                 |
| <dl> <dt>**Ungültiges nmerr- \_ \_ BLOB**</dt> </dl>                 | Das Objekt, auf das verwiesen wird, ist kein BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**nmerr- \_ Uplevel- \_ BLOB**</dt> </dl>                 | Die BLOB-Versionsnummer ist falsch.<br/>                                                                                                                                                          |
| <dl> <dt>**der nmerr- \_ \_ blobeintrag ist \_ bereits \_ vorhanden.**</dt> </dl>  | Dupliziertes BLOB.<br/>                                                                                                                                                                                |
| <dl> <dt>**der nmerr- \_ \_ blobeintrag \_ ist \_ nicht \_ vorhanden.**</dt> </dl> | Für das von *hconfigurationblob* angegebene Konfigurations-BLOB fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Zeigen Sie das von *herrorblob* zurückgegebene fehlerblob an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br/> |
| <dl> <dt>**mehrdeutiger nmerr- \_ \_ Spezifizierer**</dt> </dl>          | Die BLOB-Besitzer-oder Kategoriedaten fehlen.<br/>                                                                                                                                                    |
| <dl> <dt>**nmerr- \_ BLOB- \_ Besitzer \_ nicht \_ gefunden**</dt> </dl>       | Der Abschnitt "BLOB-Besitzer" wurde nicht gefunden.<br/>                                                                                                                                                          |
| <dl> <dt>**nmerr- \_ BLOB- \_ Kategorie \_ nicht \_ gefunden**</dt> </dl>    | Der Abschnitt "BLOB-Kategorie" wurde nicht gefunden.<br/>                                                                                                                                                       |
| <dl> <dt>**Unbekannte nmerr- \_ \_ Kategorie**</dt> </dl>             | Der Abschnitt BLOB Category wurde gefunden, aber nicht verstanden.<br/>                                                                                                                                       |
| <dl> <dt>**Unbekanntes nmerr- \_ \_ Tag**</dt> </dl>                  | Der BLOB-Tagabschnitt wurde gefunden, aber nicht verstanden.<br/>                                                                                                                                            |
| <dl> <dt>**nmerr- \_ BLOB- \_ Konvertierungs \_ Fehler**</dt> </dl>       | Das BLOB ist beschädigt.<br/>                                                                                                                                                                           |
| <dl> <dt>**nmerr-Fehler (unzulässig) \_ \_**</dt> </dl>              | Der Auslöse Teil des BLOBs ist beschädigt.<br/>                                                                                                                                                    |
| <dl> <dt>**nmerr- \_ BLOB- \_ Zeichenfolge \_ ungültig**</dt> </dl>         | Die Zeichenfolge wird nicht mit Null beendet.<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Bemerkungen

Sie müssen diese Methode anwenden, um eine NPP neu zu starten, die gestartet, beendet, aber nicht getrennt wurde.

Der von *herrorblob* zurückgegebene fehlerblob enthält Einträge, die Netzwerkmonitor in dem in *hconfigurationblob* angegebenen Konfigurations-BLOB nicht verstehen oder finden konnten. Das zurückgegebene fehlerblob enthält Fehler Daten, die von der Anwendung für die Problembehandlung verwendet werden können. Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag, Netzwerkmonitor nicht finden kann, im zurückgegebenen fehlerblob enthalten sein.

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

[BlobNetzwerkmonitor](network-monitor-blobs.md)
</dt> </dl>

 

 




