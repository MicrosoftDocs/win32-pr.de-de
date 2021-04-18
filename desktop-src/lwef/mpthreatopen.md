---
title: Mpbedrohlich Open-Funktion (mpclient. h)
description: Gibt ein enumerationshandle zum Abrufen von Bedrohungen zurück.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Mpbedrohlich Open-Funktion Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: ca30435f9d7cba32771a2445d8a1156f0edaa9b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339984"
---
# <a name="mpthreatopen-function"></a>Mpbedrohlich Open-Funktion

Gibt ein enumerationshandle zum Abrufen von Bedrohungen zurück. Diese Funktion kann verwendet werden, um von einer bestimmten Überprüfung erkannte Bedrohungen, alle aktiven Bedrohungen im System, den Verlauf der Bedrohungs Desinfektion oder alle Bedrohungen in der Signaturdatenbank zu öffnen.

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

*hscanhandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Kann ein Handle für einen abgeschlossenen Scanvorgang sein, der von der [**mpscanstart**](mpscanstart.md) -Funktion zurückgegeben wird. Alternativ kann dieser Parameter auf das von [**mpmanageropen**](mpmanageropen.md) zurückgegebene Malware Protection Manager-Schnittstellen handle festgelegt werden, um alle aktiven Bedrohungen im System, den Verlauf der Bedrohungs Desinfektion oder Bedrohungen aus der Signaturdatenbank aufzulisten.

</dd> <dt>

*Quelle* \[ in\]
</dt> <dd>

Typ: **mpthreat- \_ Quelle**

Wird verwendet, um die Quelle der Bedrohungs Aufzählung zu steuern. Die möglichen Werte für diesen Parameter sind:



| Wert                                                                                                                                                                                                 | Bedeutung                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <dt>**mpthreat- \_ Quell \_ Scan**</dt> </dl>                   | Bedrohungen, die dem jeweiligen Scan Handle zugeordnet sind.<br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <dt>**mpthreat- \_ Quelle \_ aktiv**</dt> </dl>             | Bedrohungen, die derzeit im System aktiv sind.<br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <dt>**mpthreat- \_ Quell \_ Verlauf**</dt> </dl>          | Bedrohungen, die als Verlauf behandelt und beibehalten werden.<br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <dt>**\_Quellen Quarantäne für mpthreat \_**</dt> </dl> | Bedrohungen, die unter Quarantäne gestellt werden.<br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <dt>**mpthreat- \_ Quell \_ Signatur**</dt> </dl>    | Bedrohungen, die mit der aktuellen Signaturdatenbank erkannt werden können.<br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <dt>**mpthreat- \_ Quell \_ Status**</dt> </dl>                | Bedrohungen, die vor kurzem bearbeitet wurden. ("Kürzlich" wird durch eine konfigurierbare interne Einstellung definiert.)<br/> |



 

</dd> <dt>

*Typ* \[ in\]
</dt> <dd>

Typ: **mpthreat- \_ Typ**

Wird verwendet, um aufgelistete Bedrohungen basierend auf dem Erkennungs Typ zu filtern. Die möglichen Werte für diesen Parameter sind:



| Wert                                                                                                                                                                                           | Bedeutung                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <dt>**mpthreat- \_ Typ \_ knownbad**</dt> </dl>       | Die Erkennung erfolgt basierend auf einer bestimmten Signatur, Emulation oder anderen Bedrohungs Erkennungsmethode.<br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <dt>**mpthreat- \_ Typ \_ verdächtig**</dt> </dl> | Die Erkennung erfolgt basierend auf der Verhaltens Überwachung.<br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <dt>**mpthreat- \_ Typ \_ unbekannt**</dt> </dl>          | Die Erkennung erfolgt basierend auf unbekannten Bedrohungen (nicht klassifiziert).<br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <dt>**mpthreat- \_ Typ \_ knowngood**</dt> </dl>    | Die Erkennung erfolgt basierend auf bekannten sicheren Bedrohungen.<br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <dt>**mpthreat- \_ Typ \_ NIS**</dt> </dl>                      | Die Erkennung erfolgt basierend auf NIS-Bedrohungen.<br/>                                                       |



 

</dd> <dt>

*phbedrohlich-enumhandle* \[ vorgenommen\]
</dt> <dd>

Typ: **pmphandle**

Rückgabe Handle für Bedrohungs Enumeration, das den enumerationskontext identifiziert. Dieses Handle kann zum Auflisten von Bedrohungs Informationen mithilfe von [**mpgefährenumerate**](mpthreatenumerate.md)verwendet werden. Das Handle muss mit der [**mplenker close**](mphandleclose.md) -Funktion geschlossen werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code. Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mperrormessageformat**](mperrormessageformat.md)
</dt> <dt>

[**Mplenker schließen**](mphandleclose.md)
</dt> <dt>

[**Mpmanageropen**](mpmanageropen.md)
</dt> <dt>

[**Mpscanstart**](mpscanstart.md)
</dt> <dt>

[**Mpzerenumerate**](mpthreatenumerate.md)
</dt> </dl>

 

 





