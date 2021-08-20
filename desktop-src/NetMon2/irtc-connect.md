---
description: 'IRTC::Verbinden-Methode: Die Verbinden-Methode verbindet das NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen für die Verbindung bereit.'
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: IRTC::Verbinden-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: da7ff72414a1702a1849f76f658f0fbf85116b9b831e800148d5a6165da7ac17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132899"
---
# <a name="irtcconnect-method"></a>IRTC::Verbinden-Methode

Die **Verbinden-Methode** verbindet das NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen für die Verbindung bereit.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hInputBlob* \[ In\]
</dt> <dd>

Handle für das BLOB, das die NIC angibt, mit der Sie eine Verbindung herstellen, und die Konfigurationsinformationen für diese Verbindung.

</dd> <dt>

*StatusCallbackProc* \[ In\]
</dt> <dd>

Adresse der Statusrückruffunktion des Benutzers, die Statusupdates wie Trigger empfängt. Dieser Parameter kann auf **NULL** festgelegt werden.

</dd> <dt>

*FramesCallbackProc* \[ In\]
</dt> <dd>

Adresse der Framerückruffunktion des Benutzers, die zum Empfangen von Statusaktualisierungen wie Triggern verwendet wird. Dieser Parameter kann auf **NULL** festgelegt werden.

</dd> <dt>

*UserContext* \[ In\]
</dt> <dd>

Wert, der übergeben wird, wenn der Status und die Framerückruffunktion des Benutzers aufgerufen werden. Wenn beide Rückruffunktionen angegeben werden, müssen sie denselben Benutzerkontextwert verwenden. Der Wert dieses Parameters ist in der Regel entweder HWND oder ein "this"-Zeiger.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Behandeln sie ein Fehler-BLOB, das zusätzliche Fehlerinformationen enthält. Informationen dazu, was im Fehlerblob enthalten ist, finden Sie unter Hinweise am Ende dieses Themas.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes (einschließlich der Fehler, die vom internen **IRTC::Configure-Aufruf** zurückgegeben werden):



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ BEREITS \_ VERBUNDEN**</dt> </dl>            | Diese Instanz des NPP-COM-Objekts ist bereits mit dem Netzwerk verbunden.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**\_ \_ NMERR-BLOBKONVERTIERUNGSFEHLER \_**</dt> </dl>       | Das Konfigurations-BLOB ist beschädigt. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                                       |
| <dl> <dt>**\_NMERR-BLOBEINTRAG \_ IST NICHT \_ \_ \_ VORHANDEN**</dt> </dl> | Dem durch den *Parameter hInputBlob* angegebenen Eingabe-BLOB fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Dieser Fehler kann durch den **IRTC::Verbinden-** oder **IRTC::Configure-Aufruf** generiert werden. Sehen Sie sich den von *hErrorBlob* zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br/> |
| <dl> <dt>**\_NMERR-BLOB \_ NICHT \_ INITIALISIERT**</dt> </dl>        | Die **CreateBlob-Funktion** wurde nicht aufgerufen. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                         |
| <dl> <dt>**NMERR \_ BLOB \_ STRING \_ INVALID**</dt> </dl>         | Die Zeichenfolge ist nicht NULL-terminiert. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                                       |
| <dl> <dt>**NMERR \_ ILLEGAL \_ TRIGGER**</dt> </dl>              | Der Triggerteil des Eingabeblobs ist beschädigt. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                        |
| <dl> <dt>**NMERR \_ UNGÜLTIGES \_ BLOB**</dt> </dl>                 | Das in *hInputBlob* angegebene Objekt ist kein BLOB. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                      |
| <dl> <dt>**NMERR \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>               | Der zum Ausführen dieses Vorgangs erforderliche Arbeitsspeicher ist nicht verfügbar. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                              |
| <dl> <dt>**NMERR \_ TIMEOUT**</dt> </dl>                       | Für die Anforderung ist ein Time out aufgetreten. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                                               |
| <dl> <dt>**NMERR \_ \_ UPLEVEL-BLOB**</dt> </dl>                 | Die In *hInputBlob* angegebene Versionsnummer des BLOB ist falsch. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Hinweise

Wenn die **Verbinden-Methode** aufgerufen wird, ruft das NPP automatisch die **IRTC::Configure-Methode** auf, indem das von *hInputBlob* bereitgestellte BLOB verwendet wird. Beachten Sie, dass alle Fehlercodes, die vom Aufruf von **IRTC::Configure** zurückgegeben werden, vom **IRTC::Verbinden-Aufruf** zurückgegeben werden.

Diese Methode muss aufgerufen werden, bevor Sie mit der Erfassung von Frames beginnen können. Beachten Sie Folgendes: Wenn Sie mit dieser Methode eine Verbindung mit dem Netzwerk herstellen, müssen Sie weiterhin die **IRTC-Schnittstelle** verwenden, um Frames zu erfassen.

Beim Aufrufen dieser Funktion müssen Sie einen Status oder eine Framerückruffunktion angeben, auch wenn sie nur als Platzhalter fungiert.

Das von *hInputBlob* angegebene Eingabeblob kann durch Aufrufen der Methoden **GetNPPBlobFromUI,** **GetNPPBlobTable** und **SelectNPPBlobFromTable** abgerufen werden.

Das in *hErrorBlob* zurückgegebene Fehlerblob enthält Fehlerinformationen, die der Entwickler oder die Anwendung für die Problembehandlung verwenden kann. Das von *hErrorBlob* zurückgegebene Fehlerblob enthält Einträge, die Netzwerkmonitor nicht verstehen oder im Eingabe-BLOB finden konnten, das in *hInputBlob* angegeben ist. Wenn z. B. NMERR \_ BLOB ENTRY DOES NOT EXIST zurückgegeben \_ \_ \_ \_ wird, ist der Eintrag, den Netzwerkmonitor nicht finden konnte, im zurückgegebenen Fehlerblob enthalten.



| Informationen über                          | Finden Sie unter                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Abrufen des Eingabeblobs, das eine NIC darstellt | [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Configure](irtc-configure.md)
</dt> <dt>

[IRTC::D isconnect](irtc-disconnect.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> </dl>

 

 




