---
title: Mpmanagerstatus-QUERYEX-Funktion (mpclient. h)
description: Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück. | Mpmanagerstatus-QUERYEX-Funktion (mpclient. h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Mpmanagerstatus-QUERYEX-Funktion Legacy Features der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361173"
---
# <a name="mpmanagerstatusqueryex-function"></a>Mpmanagerstatus-QUERYEX-Funktion

Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hmphandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Handle für die Malware Protection Manager-Schnittstelle. Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.

</dd> <dt>

*dwFlag* \[ in\]
</dt> <dd>

Typ: **DWORD**

Steuert, welche Abfrage Informationen zurückgegeben werden. Einige Informationen sind aufwendig und werden möglicherweise nicht benötigt.



| Wert                                                                                                                                                                                                         | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <dt>**MP- \_ Status \_ Abfrage Flags " \_ \_ None"**</dt> </dl>       | Standard.<br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <dt>**MP \_ - \_ statusabfrageflag \_ \_ nostate**</dt> </dl> | Keine Abfrage von Zustandsinformationen.<br/> |



 

</dd> <dt>

*pstatusinfo* \[ vorgenommen\]
</dt> <dd>

Typ: **pmpstatus- \_ Informationen**

Zeiger auf eine-Struktur, die Statusinformationen zu den letzten Scans, aktiven Bedrohungen und verschiedenen Komponenten Status zurückgibt. Siehe [**mpstatus- \_ Informationen**](mpstatus-info.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**. Dieser Funktions Aufrufvorgang ist garantiert auch dann erfolgreich, wenn kein antischadsoftwaredienst ausgeführt wird.

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

[**Mpmanageropen**](mpmanageropen.md)
</dt> <dt>

[**mpstatus- \_ Informationen**](mpstatus-info.md)
</dt> </dl>

 

 





