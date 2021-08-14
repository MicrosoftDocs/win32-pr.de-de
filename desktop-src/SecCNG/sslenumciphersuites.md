---
description: Listet die Verschlüsselungssammlungen auf, die von einem SSL-Protokollanbieter (Secure Sockets Layer Protocol) unterstützt werden.
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: SslEnumCipherSuites-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7d9fb40bf6bfebff6d0659640dfb68b718586ac822c8a779a56de300b8d55b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906692"
---
# <a name="sslenumciphersuites-function"></a>SslEnumCipherSuites-Funktion

Die **SslEnumCipherSuites-Funktion** listet die Verschlüsselungssammlungen auf, die von einem SSL-Protokollanbieter [*(Secure Sockets Layer Protocol)*](/windows/desktop/SecGloss/s-gly) unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der SSL-Protokollanbieterinstanz.

</dd> <dt>

*hPrivateKey* \[ in, optional\]
</dt> <dd>

Das Handle eines [*privaten Schlüssels.*](/windows/desktop/SecGloss/p-gly) Wenn ein privater Schlüssel angegeben wird, listet **SslEnumCipherSuites** die Verschlüsselungssammlungen auf, die mit dem privaten Schlüssel kompatibel sind. Wenn der private Schlüssel beispielsweise ein DSS-Schlüssel ist, werden nur die DSS \_ DHE-Verschlüsselungssammlungen zurückgegeben. Wenn der private Schlüssel ein RSA-Schlüssel ist, aber keine unformatierten Entschlüsselungsvorgänge unterstützt, werden die SSL2-Verschlüsselungssammlungen nicht zurückgegeben.

Legen Sie diesen Parameter auf **NULL** fest, wenn Sie keinen privaten Schlüssel angeben.

> [!Note]  
> Ein *hPrivateKey-Handle* wird durch Aufrufen der [**SslOpenPrivateKey-Funktion**](sslopenprivatekey.md) abgerufen. Handles, die von der [**NCryptOpenKey-Funktion**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) abgerufen werden, werden nicht unterstützt.

 

</dd> <dt>

*ppCipherSuite* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**NCRYPT \_ SSL \_ CIPHER \_ SUITE-Struktur,**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) um die Adresse der nächsten Verschlüsselungssammlung in der Liste zu empfangen.

</dd> <dt>

*ppEnumState* \[ in, out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die aktuelle Position in der Liste der Verschlüsselungssammlungen angibt.

Legen Sie den Zeiger beim ersten Aufruf von **SslEnumCipherSuites** auf **NULL** fest. Übergeben Sie bei jedem nachfolgenden Aufruf den unveränderten Wert zurück an **SslEnumCipherSuites.**

Wenn keine Verschlüsselungssammlungen mehr verfügbar sind, sollten Sie *ppEnumState* freigeben, indem Sie die [**SslFreeBuffer-Funktion**](sslfreebuffer.md) aufrufen.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>      | Es ist nicht genügend Arbeitsspeicher verfügbar, um die erforderlichen Puffer zuzuordnen.<br/> |
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl> | Einer der bereitgestellten Handles ist ungültig.<br/>                     |
| <dl> <dt>**NTE \_ NO \_ MORE \_ ITEMS**</dt> <dt>0x8009002AL</dt> </dl> | Es werden keine zusätzlichen Verschlüsselungssammlungen unterstützt.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Um alle vom SSL-Anbieter unterstützten Verschlüsselungssammlungen aufzuzählen, rufen Sie die **SslEnumCipherSuites-Funktion** in einer Schleife auf, bis **NTE \_ NO MORE \_ \_ ITEMS** zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Ncrypt.lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**NCRYPT \_ SSL \_ CIPHER \_ SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

