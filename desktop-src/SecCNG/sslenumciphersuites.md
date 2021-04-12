---
description: Listet die Verschlüsselungs Sammlungen auf, die von einem Protokoll Anbieter für Secure Sockets Layer Protokoll (SSL) unterstützt werden.
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: Sslenenciphersuites-Funktion (sslprovider. h)
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
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345039"
---
# <a name="sslenumciphersuites-function"></a>Sslenenciphersuites-Funktion

Die Funktion **sslenumciphersuites** listet die Verschlüsselungs Sammlungen auf, die von einem Protokoll Anbieter für [*Secure Sockets Layer Protokoll*](/windows/desktop/SecGloss/s-gly) (SSL) unterstützt werden.

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der SSL-Protokoll Anbieter Instanz.

</dd> <dt>

*hprivatekey* \[ in, optional\]
</dt> <dd>

Das Handle eines [*privaten Schlüssels*](/windows/desktop/SecGloss/p-gly). Wenn ein privater Schlüssel angegeben wird, listet **sslenumciphersuites** die Verschlüsselungs Sammlungen auf, die mit dem privaten Schlüssel kompatibel sind. Wenn der private Schlüssel z. b. ein DSS-Schlüssel ist, werden nur die DSS dit-Verschlüsselungs Sammlungen \_ zurückgegeben. Wenn der private Schlüssel ein RSA-Schlüssel ist, aber keine unformatierten Entschlüsselungs Vorgänge unterstützt, werden die SSL2 verwendet-Verschlüsselungs Sammlungen nicht zurückgegeben.

Legen Sie diesen Parameter auf **null** fest, wenn Sie keinen privaten Schlüssel angeben.

> [!Note]  
> Ein *hprivatekey* -Handle wird durch Aufrufen der [**sslopenprivatekey**](sslopenprivatekey.md) -Funktion abgerufen. Handles, die von der [**ncryptopenkey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) -Funktion abgerufen werden, werden nicht unterstützt.

 

</dd> <dt>

*ppciphersuite* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**NCrypt- \_ SSL- \_ Chiffre \_**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) Sammlungs Struktur, die die Adresse der nächsten Verschlüsselungs Sammlung in der Liste empfängt.

</dd> <dt>

" *ppumschlag State* \[ " in, out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die aktuelle Position in der Liste der Verschlüsselungs Sammlungen angibt.

Legen Sie den Zeiger beim ersten **sslenumciphersuites**-aufrufswert auf **null** fest. Übergeben Sie bei jedem nachfolgenden-Rückruf den nicht geänderten Wert zurück an **sslenenciphersuites**.

Wenn keine weiteren Verschlüsselungs Sammlungen verfügbar sind, sollten Sie " *pprestate* " durch Aufrufen der Funktion " [**sslfreebuffer**](sslfreebuffer.md) " freigeben.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt> </dl>      | Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.<br/> |
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl> | Eines der bereitgestellten Handles ist ungültig.<br/>                     |
| <dl> <dt>**Ernte \_ Keine \_ weiteren \_ Elemente**</dt> <dt>0x8009002al</dt> </dl> | Es werden keine zusätzlichen Verschlüsselungs Sammlungen unterstützt.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Um alle Verschlüsselungs Sammlungen aufzulisten, die vom SSL-Anbieter unterstützt werden, müssen Sie die **sslenumciphersuites** -Funktion in einer Schleife aufzurufen, bis die **\_ \_ \_ Elemente nicht mehr** zurückgegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Ncrypt. lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ncrypt-SSL-Verschlüsselungs \_ \_ \_ Sammlung**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

