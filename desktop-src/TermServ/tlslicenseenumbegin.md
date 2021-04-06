---
title: Tlslicenseenumbegin-Funktion
description: Beginnt die Enumeration von Lizenzen, die vom Remotedesktop Lizenzserver basierend auf Suchkriterien ausgestellt werden.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- Tlslicenseenumbegin-Funktion Remotedesktopdienste
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
ms.openlocfilehash: 95913337de968d0b30780b5898b7f204d947dd4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743608"
---
# <a name="tlslicenseenumbegin-function"></a>Tlslicenseenumbegin-Funktion

Beginnt die Enumeration von Lizenzen, die vom Remotedesktop Lizenzserver basierend auf Suchkriterien ausgestellt werden.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.

 

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

*hHandle* \[ in\]
</dt> <dd>

Handle für einen Remotedesktop-Lizenzserver. Geben Sie ein Handle an, das von der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet wird.

</dd> <dt>

*dwsearchparser* \[ in\]
</dt> <dd>

Gibt die Suchkriterien an. Der-Parameter kann eine oder eine Kombination der Werte sein, die in der folgenden Liste beschrieben werden. Der-Parameter gibt den Typ des Schlüssel Pakets und das zu durchsuchende Key Pack an.

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**Lslicense \_ Durchsuchen von \_ licenseid** (0x00000001)


</dt> <dd>

Suchen Sie nach Lizenz-ID.

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**Lslicense \_ \_Keypackid suchen** (0x00000002)


</dt> <dd>

Suchen Sie nach Key Pack-ID.

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**Lslicense \_ \_MachineName suchen** (0x00000008)


</dt> <dd>

Nach Computernamen suchen.

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**Lslicense \_ \_Benutzername suchen** (0x00000010)


</dt> <dd>

Suchen Sie nach Benutzername.

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**Lslicense \_ Suche \_ IssueDate** (0x00000080)


</dt> <dd>

Nach Ausgabedatum suchen.

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**Lslicense \_ Durchsuchen von \_ ExpireDate** (0x00000100)


</dt> <dd>

Nach Ablaufdatum suchen.

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**Lslicense \_ \_ Numlicenses suchen** (0x00000200)


</dt> <dd>

Suchen Sie nach Anzahl der Lizenzen.

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**Lslicense \_ Such \_ Eintrags \_ Status** (0x20000000)


</dt> <dd>

Nach Eintrags Status suchen.

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**Lslicense \_ ExSearch \_ licenstatusstatus** (0x00100000)


</dt> <dd>

Suchen Sie nach Lizenzstatus.

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**Lschräypack \_ \_Alle suchen** (0xFFFFFFFF)


</dt> <dd>

Alle Lizenzen suchen.

</dd> </dl> </dd> <dt>

*bmatchall* \[ in\]
</dt> <dd>

Gibt an, ob alle Suchwerte abgeglichen werden sollen.

</dd> <dt>

*lpsearchparameminm* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**lslicense**](lslicense.md) -Struktur, die die Suchparameter angibt, nach denen gesucht werden soll.

</dd> <dt>

*pdwerrcode* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die bei der Rückgabe einen der folgenden Fehlercodes empfängt.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ S \_ erfolgreich** (0)


</dt> <dd>

Der-Vorgang wurde erfolgreich ausgeführt.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Lserver \_ Interner E- \_ \_ Fehler** (5001)


</dt> <dd>

Interner Fehler auf dem Lizenzserver.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Lserver \_ E \_ ungültige \_ Reihenfolge** (5006)


</dt> <dd>

Die Aufruf Sequenz war nicht gültig. Höchstwahrscheinlich wurde eine vorherige Enumeration nicht beendet.

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Lserver \_ E- \_ Server \_ ausgelastet** (5007)


</dt> <dd>

Der Lizenzserver ist zu stark ausgelastet, um die Anforderung zu verarbeiten.

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Lserver \_ E \_ outo-Memory** (5008)


</dt> <dd>

Die Anforderung kann aufgrund von unzureichendem Arbeitsspeicher nicht verarbeitet werden.

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**Lserver \_ E \_ ungültige \_ Daten** (5009)


</dt> <dd>

Die Daten im Suchparameter sind ungültig.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt die folgenden möglichen Rückgabewerte zurück.

<dl> <dt>

**RPC \_ S \_ OK**
</dt> <dd>

Der-Befehl wurde erfolgreich ausgeführt. Überprüfen Sie den Wert des Parameters " *pdwerrcode* ", um den Rückgabecode für den-Befehl abzurufen.

</dd> <dt>

**RPC \_ S \_ ungültig \_**
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

[**Lslicense**](lslicense.md)
</dt> <dt>

[**Tlsconnecttolsserver**](tlsconnecttolsserver.md)
</dt> <dt>

[**Tlslicensitztenenumnext**](tlslicenseenumnext.md)
</dt> <dt>

[**Tlslicenabenumend**](tlslicenseenumend.md)
</dt> </dl>

 

