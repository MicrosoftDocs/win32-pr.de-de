---
title: MpThreatOpen-Funktion (MpClient.h)
description: Gibt ein Enumerationshand handle zum Abrufen von Bedrohungen zurück.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- MpThreatOpen-Funktion Legacy Windows Umgebungsfeatures
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949fd1c8291ecb183cf51cf5385fe356a33cb1288978fda42f37d748f1a162a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746889"
---
# <a name="mpthreatopen-function"></a>MpThreatOpen-Funktion

Gibt ein Enumerationshand handle zum Abrufen von Bedrohungen zurück. Diese Funktion kann verwendet werden, um Bedrohungen zu öffnen, die von einer bestimmten Überprüfung erkannt wurden, alle aktiven Bedrohungen im System, den Verlauf der Bedrohungsbedrohung oder alle Bedrohungen, die in der Signaturdatenbank vorhanden sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hScanHandle* \[ In\]
</dt> <dd>

Typ: **MPHANDLE**

Kann ein Handle für einen abgeschlossenen Scanvorgang sein, der von der [**MpScanStart-Funktion zurückgegeben**](mpscanstart.md) wird. Alternativ kann dieser Parameter auf das Handle der Malware Protection Manager-Schnittstelle festgelegt werden, das von [**MpManagerOpen**](mpmanageropen.md) zurückgegeben wird, um alle aktiven Bedrohungen im System, den Verlauf der Bedrohungsbedrohung oder Bedrohungen aus der Signaturdatenbank aufzählen zu können.

</dd> <dt>

*ThreatSource* \[ In\]
</dt> <dd>

Typ: **MPTHREAT \_ SOURCE**

Wird verwendet, um die Quelle der Bedrohungsenumeration zu steuern. Die möglichen Werte für diesen Parameter sind:



| Wert                                                                                                                                                                                                 | Bedeutung                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <dt>**\_MPTHREAT-QUELLSCAN \_**</dt> </dl>                   | Bedrohungen, die dem spezifischen Überprüfungshand handle zugeordnet sind.<br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <dt>**MPTHREAT \_ SOURCE \_ ACTIVE**</dt> </dl>             | Bedrohungen, die derzeit im System aktiv sind.<br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <dt>**\_MPTHREAT-QUELLVERLAUF \_**</dt> </dl>          | Bedrohungen, die als Verlauf umgesetzt und beibehalten werden.<br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <dt>**\_MPTHREAT-QUELLQUARANTÄNE \_**</dt> </dl> | Bedrohungen, die unter Quarantäne gestellt werden.<br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <dt>**\_MPTHREAT-QUELLSIGNATUR \_**</dt> </dl>    | Bedrohungen, die mit der aktuellen Signaturdatenbank erkannt werden können.<br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <dt>**\_MPTHREAT-QUELLZUSTAND \_**</dt> </dl>                | Bedrohungen, auf die vor Kurzem reagiert wurde. ("Recently" wird durch eine konfigurierbare interne Einstellung definiert.)<br/> |



 

</dd> <dt>

*ThreatType* \[ In\]
</dt> <dd>

Typ: **MPTHREAT \_ TYPE**

Wird verwendet, um aufzählte Bedrohungen basierend auf dem Erkennungstyp zu filtern. Die möglichen Werte für diesen Parameter sind:



| Wert                                                                                                                                                                                           | Bedeutung                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <dt>**MPTHREAT-TYP \_ \_ KNOWNBAD**</dt> </dl>       | Die Erkennung erfolgt basierend auf einer bestimmten Signatur, Emulation oder einer anderen Bedrohungserkennungsmethode.<br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <dt>**MPTHREAT-TYP \_ VERDÄCHTIG \_**</dt> </dl> | Die Erkennung erfolgt basierend auf der Verhaltensüberwachung.<br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <dt>**MPTHREAT-TYP \_ \_ UNBEKANNT**</dt> </dl>          | Die Erkennung erfolgt basierend auf unbekannten Bedrohungen (nicht klassifiziert).<br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <dt>**MPTHREAT-TYP \_ \_ KNOWNGOOD**</dt> </dl>    | Die Erkennung erfolgt basierend auf bekannten sicheren Bedrohungen.<br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <dt>**MPTHREAT \_ TYPE \_ NIS**</dt> </dl>                      | Die Erkennung erfolgt basierend auf NIS-Bedrohungen.<br/>                                                       |



 

</dd> <dt>

*phThreatEnumHandle* \[ out\]
</dt> <dd>

Typ: **PMPHANDLE**

Zurückgegebenes Bedrohungsenumerationshand handle, das den Enumerationskontext identifiziert. Dieses Handle kann zum Aufzählen von Bedrohungsinformationen mit [**mpThreatEnumerate verwendet werden.**](mpthreatenumerate.md) Das Handle muss mit der [**MpHandleClose-Funktion geschlossen**](mphandleclose.md) werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **S \_ OK.**

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT-Code.** Der Aufrufer kann die [**MpErrorMessageFormat-Funktion**](mperrormessageformat.md) verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> </dl>

 

 





