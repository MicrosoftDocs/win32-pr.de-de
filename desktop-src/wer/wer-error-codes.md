---
title: Wer-Fehler Codes (werapi. h)
description: Die folgende Tabelle enthält eine Liste mit benutzerdefinierten Fehlercodes, die von Windows-Fehlerberichterstattung verwendet werden.
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341379"
---
# <a name="wer-error-codes"></a>Wer-Fehler Codes

Die folgende Tabelle enthält eine Liste mit benutzerdefinierten Fehlercodes, die von Windows-Fehlerberichterstattung verwendet werden.



| Konstante                                                                                                                                                                                            | BESCHREIBUNG                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <dt>**\_ \_ nicht genügend \_ Puffer**</dt> </dl> | Ein Puffer ist zu klein, um die Daten zu enthalten.<br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <dt>**\_ \_ ungültiger \_ Status**</dt> </dl>                   | Eine Funktion wurde in einer nicht unterstützten Weise aufgerufen.<br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <dt>**Länge von wer \_ E \_ \_ überschritten**</dt> </dl>             | Eine der Längen Limits wurde überschritten.<br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <dt>**Wer \_ E \_ fehlt \_ param.**</dt> </dl>                   | Mindestens ein Parameter fehlt.<br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <dt>**Wer \_ E \_ nicht \_ gefunden hat.**</dt> </dl>                               | Element wurde nicht gefunden.<br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <dt>**Wer \_ E \_ Store \_ deaktiviert**</dt> </dl>                | Der Speicher wurde deaktiviert.<br/>                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Werapi. h</dt> </dl> |



 

 





