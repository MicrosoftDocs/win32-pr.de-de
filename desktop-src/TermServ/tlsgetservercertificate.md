---
title: Tlsgetservercertificate-Funktion
description: Gibt das Zertifikat des Remotedesktop Lizenzservers zurück.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- Tlsgetservercertificate-Funktion Remotedesktopdienste
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3144245863ee4a4316bbce8333f03ca3901cb499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338130"
---
# <a name="tlsgetservercertificate-function"></a>Tlsgetservercertificate-Funktion

Gibt das Zertifikat des Remotedesktop Lizenzservers zurück.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mstlsapi.dll zu verknüpfen.

 

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hHandle* \[ in\]
</dt> <dd>

Handle für einen Remotedesktop Lizenzserver, der durch einen Rückruf der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion geöffnet wird.

</dd> <dt>

*bsigncert* \[ in\]
</dt> <dd>

**True** , wenn das Signaturzertifikat **false** ist, wenn Exchange-Zertifikat.

</dd> <dt>

*ppbcertblob* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Zeiger auf einen Puffer empfängt, der das Zertifikat enthält.

</dd> <dt>

*lpdwcertbloblen* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Zertifikats erhält, das zurückgegeben wird.

</dd> <dt>

*pdwerrcode* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den Fehlercode empfängt.

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ S \_ erfolgreich** (0)


</dt> <dd>

Der-Vorgang wurde erfolgreich ausgeführt.

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS \_ W- \_ selfsign- \_ Zertifikat** (4007)


</dt> <dd>

Das zurückgegebene Zertifikat ist ein selbst signiertes Zertifikat.

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS \_ W \_ Temp \_ selfsign- \_ Zertifikat** (4009)


</dt> <dd>

Das zurückgegebene Zertifikat ist temporär.

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS \_ E- \_ Zugriff \_ verweigert** (5003)


</dt> <dd>

Zugriff verweigert.

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS \_ E Zuordnungs \_ \_ handle** (5007)


</dt> <dd>

Der Server ist zu stark ausgelastet, um die Anforderung zu verarbeiten.

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS \_ E \_ kein \_ Zertifikat** (5022)


</dt> <dd>

Ein Zertifikat kann nicht abgerufen werden.

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

[**Tlsconnecttolsserver**](tlsconnecttolsserver.md)
</dt> </dl>

 

