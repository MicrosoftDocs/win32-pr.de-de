---
title: TLSLicenseEnumBegin-Funktion
description: Beginnt die Enumeration von Lizenzen, die vom lizenzbasierten Remotedesktop basierend auf Suchkriterien ausgestellt werden.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- TLSLicenseEnumBegin-Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620f6487bb516a76ac5cb7f77da9983178933c24ac03151bd9a4c8455f694ec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986880"
---
# <a name="tlslicenseenumbegin-function"></a>TLSLicenseEnumBegin-Funktion

Beginnt die Enumeration von Lizenzen, die vom lizenzbasierten Remotedesktop basierend auf Suchkriterien ausgestellt werden.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mstlsapi.dll.

 

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hHandle* \[ In\]
</dt> <dd>

Handle für einen Remotedesktop Lizenzserver. Geben Sie ein Handle an, das von der [**TLSConnectToLsServer-Funktion geöffnet**](tlsconnecttolsserver.md) wird.

</dd> <dt>

*dwSearchParm* \[ In\]
</dt> <dd>

Gibt die Suchkriterien an. Der -Parameter kann eine oder eine Kombination der In der folgenden Liste beschriebenen Werte sein. Der -Parameter gibt den Typ des Schlüsselpakets und das zu durchsuchende Schlüsselpaket an.

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_ SEARCH \_ LICENSEID** (0x00000001)


</dt> <dd>

Suchen Sie nach der Lizenz-ID.

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_ SEARCH \_ KEYPACKID** (0x00000002)


</dt> <dd>

Suchen Sie nach der Schlüsselpaket-ID.

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_ SEARCH \_ MACHINENAME** (0x00000008)


</dt> <dd>

Suchen Sie nach dem Computernamen.

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_ BENUTZERNAME \_ SUCHEN** (0x00000010)


</dt> <dd>

Suchen Sie nach Benutzername.

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_ SEARCH \_ ISSUEDATE** (0X00000080)


</dt> <dd>

Suchen Sie nach Dem Problemdatum.

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_ SEARCH \_ EXPIREDATE** (0x00000100)


</dt> <dd>

Suche nach Ablaufdatum.

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_ \_ NUMLICENSES DURCHSUCHEN** (0x00000200)


</dt> <dd>

Suchen Sie nach der Anzahl der Lizenzen.

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_ \_ \_ SUCHEINTRAGSSTATUS** (0X20000000)


</dt> <dd>

Suchen Sie nach dem Eintragsstatus.

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_ EXSEARCH \_ LICENSESTATUS** (0x00100000)


</dt> <dd>

Suchen Sie nach lizenzstatus.

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_ SEARCH \_ ALL** (0xFFFFFFFF)


</dt> <dd>

Durchsuchen Sie alle Lizenzen.

</dd> </dl> </dd> <dt>

*bMatchAll* \[ In\]
</dt> <dd>

Gibt an, ob alle Suchwerte übereinstimmen.

</dd> <dt>

*lpSearchParm* \[ In\]
</dt> <dd>

Zeiger auf eine [**LSLicense-Struktur,**](lslicense.md) die die Suchparameter angibt, nach denen gesucht werden soll.

</dd> <dt>

*pdwErrCode* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die bei der Rückgabe einen der folgenden Fehlercodes empfängt.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_ S \_ SUCCESS** (0)


</dt> <dd>

Der Aufruf ist erfolgreich.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_ INTERNER \_ \_ E-FEHLER** (5001)


</dt> <dd>

Interner Fehler auf dem Lizenzserver.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_ E \_ \_ UNGÜLTIGE SEQUENZ** (5006)


</dt> <dd>

Die aufrufende Sequenz war ungültig. Höchstwahrscheinlich wurde eine vorherige Enumeration nicht beendet.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_ E \_ SERVER \_ AUSGELASTET** (5007)


</dt> <dd>

Der Lizenzserver ist zu ausgelastet, um die Anforderung zu verarbeiten.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_ E \_ OUTOFMEMORY** (5008)


</dt> <dd>

Die Anforderung kann aufgrund von unzureichendem Arbeitsspeicher nicht verarbeitet werden.

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_ E \_ \_ UNGÜLTIGE DATEN** (5009)


</dt> <dd>

Daten im Suchparameter sind ungültig.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt die folgenden möglichen Rückgabewerte zurück.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

Der Aufruf war erfolgreich. Überprüfen Sie den Wert des *pdwErrCode-Parameters,* um den Rückgabecode für den Aufruf zu erhalten.

</dd> <dt>

**RPC \_ S \_ INVALID \_ ARG**
</dt> <dd>

Das Argument war ungültig.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LSLicense**](lslicense.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

