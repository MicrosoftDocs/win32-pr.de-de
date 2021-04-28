---
description: 'IRTC::Connect-Methode: Die Connect-Methode verbindet das NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen für die Verbindung zur Verfügung.'
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: IRTC::Connect-Methode (Netmon.h)
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
ms.openlocfilehash: ba62f3341b18ddfdbf09af4eec701322d901ab79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110744"
---
# <a name="irtcconnect-method"></a>IRTC::Connect-Methode

Die **Connect-Methode** verbindet den NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen für die Verbindung zur Verfügung.

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

Handle für das BLOB, das die NIC angibt, mit der Sie eine Verbindung herstellen, und die Konfigurationsinformationen für diese Verbindung angibt.

</dd> <dt>

*StatusCallbackProc* \[ In\]
</dt> <dd>

Adresse der Statusrückruffunktion des Benutzers, die Statusupdates wie Trigger empfängt. Dieser Parameter kann auf NULL **festgelegt werden.**

</dd> <dt>

*FramesCallbackProc* \[ In\]
</dt> <dd>

Adresse der Framerückruffunktion des Benutzers, die zum Empfangen von Statusupdates wie Triggern verwendet wird. Dieser Parameter kann auf NULL **festgelegt werden.**

</dd> <dt>

*UserContext* \[ In\]
</dt> <dd>

Der Wert wird übergeben, wenn der Status und die Framerückruffunktion des Benutzers aufgerufen werden. Wenn beide Rückruffunktionen angegeben werden, müssen sie denselben Benutzerkontextwert verwenden. Der Wert dieses Parameters ist in der Regel entweder HWND oder ein This-Zeiger.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Handle für ein Fehlerblob, das zusätzliche Fehlerinformationen enthält. Informationen dazu, was im Fehlerblob enthalten ist, finden Sie unter Hinweise am Ende dieses Themas.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes (einschließlich der Fehler, die vom internen **IRTC::Configure-Aufruf** zurückgegeben werden):



| Rückgabecode                                                                                                         | Beschreibung                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ BEREITS \_ VERBUNDEN**</dt> </dl>            | Diese Instanz des NPP-COM-Objekts ist bereits mit dem Netzwerk verbunden.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**\_ \_ NMERR-BLOBKONVERTIERUNGSFEHLER \_**</dt> </dl>       | Das Konfigurations-BLOB ist beschädigt. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                                       |
| <dl> <dt>**NMERR \_ BLOB ENTRY DOES NOT EXIST (NMERR-BLOBEINTRAG IST NICHT \_ \_ \_ \_ VORHANDEN)**</dt> </dl> | Dem durch den *hInputBlob-Parameter* angegebenen Eingabeblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist. Dieser Fehler kann durch den **IRTC::Connect-** oder **IRTC::Configure-Aufruf** generiert werden. Sehen Sie sich den von *hErrorBlob* zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.<br/> |
| <dl> <dt>**\_NMERR-BLOB \_ NICHT \_ INITIALISIERT**</dt> </dl>        | Die **CreateBlob-Funktion** wurde nicht aufgerufen. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                         |
| <dl> <dt>**NMERR \_ BLOB \_ STRING \_ INVALID**</dt> </dl>         | Die Zeichenfolge ist nicht NULL-terminiert. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                                       |
| <dl> <dt>**NMERR \_ ILLEGAL \_ TRIGGER**</dt> </dl>              | Der Triggerteil des Eingabeblobs ist beschädigt. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                        |
| <dl> <dt>**NMERR \_ UNGÜLTIGES \_ BLOB**</dt> </dl>                 | Das in *hInputBlob* angegebene Objekt ist kein BLOB. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                      |
| <dl> <dt>**NMERR \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt> </dl>               | Der zum Ausführen dieses Vorgangs erforderliche Arbeitsspeicher ist nicht verfügbar. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                              |
| <dl> <dt>**NMERR \_ TIMEOUT**</dt> </dl>                       | Für die Anforderung ist ein Time out aufgetreten. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                                                               |
| <dl> <dt>**\_ \_ NMERR-UPLEVEL-BLOB**</dt> </dl>                 | Die In *hInputBlob* angegebene Versionsnummer des BLOB ist falsch. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Wenn die **Connect-Methode** aufgerufen wird, ruft das NPP automatisch die **IRTC::Configure-Methode** auf, indem das von *hInputBlob* bereitgestellte BLOB verwendet wird. Beachten Sie, dass alle Fehlercodes, die vom Aufruf von **IRTC::Configure** zurückgegeben werden, zurückgegeben und vom **IRTC::Connect-Aufruf** zurückgegeben werden.

Diese Methode muss aufgerufen werden, bevor Sie mit der Erfassung von Frames beginnen können. Beachten Sie Folgendes: Wenn Sie mit dieser Methode eine Verbindung mit dem Netzwerk herstellen, müssen Sie weiterhin die **IRTC-Schnittstelle** verwenden, um Frames zu erfassen.

Beim Aufrufen dieser Funktion müssen Sie einen Status oder eine Framerückruffunktion angeben, auch wenn sie nur als Platzhalter fungiert.

Das von *hInputBlob* angegebene Eingabeblob kann durch Aufrufen der Methoden **GetNPPBlobFromUI,** **GetNPPBlobTable** und **SelectNPPBlobFromTable** abgerufen werden.

Das in *hErrorBlob* zurückgegebene Fehlerblob enthält Fehlerinformationen, die der Entwickler oder die Anwendung für die Problembehandlung verwenden kann. Das von *hErrorBlob* zurückgegebene Fehlerblob enthält Einträge, die Netzwerkmonitor nicht verstehen oder im Eingabe-BLOB finden konnten, das in *hInputBlob* angegeben ist. Wenn z. B. NMERR \_ BLOB ENTRY DOES NOT EXIST zurückgegeben \_ \_ \_ \_ wird, ist der Eintrag, den Netzwerkmonitor nicht finden konnte, im zurückgegebenen Fehlerblob enthalten.



| Informationen über                          | Finden Sie unter                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Abrufen des Eingabeblobs, das eine NIC darstellt | [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Configure](irtc-configure.md)
</dt> <dt>

[IRTC::D isconnect](irtc-disconnect.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> </dl>

 

 




