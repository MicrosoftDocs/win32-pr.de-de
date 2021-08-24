---
title: MpManagerStatusQueryEx-Funktion (MpClient.h)
description: Gibt Statusinformationen zu verschiedenen Komponenten des Schadsoftwareschutz-Managers zurück. | MpManagerStatusQueryEx-Funktion (MpClient.h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- MpManagerStatusQueryEx-Funktion Legacy Windows Umgebungsfeatures
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
ms.openlocfilehash: d8d7e3e6135a5f01691528480b760cfea422c78b9c032219f6e100da5ebd929d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961110"
---
# <a name="mpmanagerstatusqueryex-function"></a>MpManagerStatusQueryEx-Funktion

Gibt Statusinformationen zu verschiedenen Komponenten des Schadsoftwareschutz-Managers zurück.

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

*hMpHandle* \[ In\]
</dt> <dd>

Typ: **MPHANDLE**

Handle für die Benutzeroberfläche des Schadsoftwareschutz-Managers. Dieses Handle wird von der [**MpManagerOpen-Funktion**](mpmanageropen.md) zurückgegeben.

</dd> <dt>

*dwFlag* \[ In\]
</dt> <dd>

Typ: **DWORD**

Steuert, welche Abfrageinformationen zurückgegeben werden. Einige Informationen sind teuer und werden möglicherweise nicht benötigt.



| Wert                                                                                                                                                                                                         | Bedeutung                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <dt>**MP \_ STATUS \_ QUERY \_ FLAGS \_ NONE**</dt> </dl>       | Standard.<br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <dt>**MP \_ STATUS \_ QUERY \_ FLAG \_ NOSTATE**</dt> </dl> | Fragen Sie keine Zustandsinformationen ab.<br/> |



 

</dd> <dt>

*pStatusInfo* \[ out\]
</dt> <dd>

Typ: **PMPSTATUS \_ INFO**

Zeiger auf eine -Struktur, die Statusinformationen zu letzten Scans, aktiven Bedrohungen und verschiedenen Komponentenstatus zurückgibt. Weitere Informationen [**finden Sie unter MPSTATUS \_ INFO**](mpstatus-info.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **S \_ OK.** Dieser Funktionsaufruf ist auch dann erfolgreich, wenn kein AntiMalware-Dienst ausgeführt wird.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT-Code.** Der Aufrufer kann die [**MpErrorMessageFormat-Funktion**](mperrormessageformat.md) verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**\_MPSTATUS-INFORMATIONEN**](mpstatus-info.md)
</dt> </dl>

 

 





