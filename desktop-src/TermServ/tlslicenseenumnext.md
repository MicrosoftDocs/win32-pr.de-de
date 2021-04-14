---
title: Tlslicensenumnext-Funktion
description: Wird von einem vorherigen aufrufsvorgang der tlslicenseenumbegin-Funktion fortgesetzt und gibt die nächste Lizenz zurück, die auf einem Remotedesktop Lizenzserver installiert ist, der den Suchkriterien entspricht.
ms.assetid: 6932289b-b59c-493c-8dbc-03c0662e921e
ms.tgt_platform: multiple
keywords:
- Tlslicensenumnext-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSLicenseEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c13b0a3137258015fe311c49b2cc9b999e3a13f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392210"
---
# <a name="tlslicenseenumnext-function"></a>Tlslicensenumnext-Funktion

Wird von einem vorherigen aufrufsvorgang der [**tlslicenseenumbegin**](tlslicenseenumbegin.md) -Funktion fortgesetzt und gibt die nächste Lizenz zurück, die auf einem Remotedesktop Lizenzserver installiert ist, der den Suchkriterien entspricht.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI TLSLicenseEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LSLicense  *lpLicense,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hHandle* \[ in\]
</dt> <dd>

Handle für einen Remotedesktop-Lizenzserver. Geben Sie ein Handle an, das von der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet wird.

</dd> <dt>

*lplicense* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**lslicense**](lslicense.md) -Struktur, die die nächste Lizenz empfängt, die den Suchkriterien entspricht.

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

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**Lserver \_ \_Keine \_ weiteren \_ Daten** (4001)


</dt> <dd>

Keine weiteren Lizenzen stimmen mit den Suchkriterien überein.

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Lserver \_ Interner E- \_ \_ Fehler** (5001)


</dt> <dd>

Interner Fehler auf dem Lizenzserver.

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Lserver \_ E \_ ungültige \_ Reihenfolge** (5006)


</dt> <dd>

Die Aufruf Sequenz war nicht gültig. Vor diesem muss die [**tlslicenseenumbegin ()**](tlslicenseenumbegin.md) -Funktion aufgerufen werden.

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

[**Tlslicenseenumbegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**Tlslicenabenumend**](tlslicenseenumend.md)
</dt> </dl>

 

