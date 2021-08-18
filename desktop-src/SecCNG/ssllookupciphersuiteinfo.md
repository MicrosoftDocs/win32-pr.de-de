---
description: Ruft die Verschlüsselungssammlungsinformationen für ein angegebenes Protokoll, eine Verschlüsselungssammlung und einen Schlüsseltypsatz ab.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: SslLookupCipherSuiteInfo-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherSuiteInfo
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bf56f199ae0d367517558a12a0e84bf8ce26e7bdf5f70625b878066152d0b696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905609"
---
# <a name="ssllookupciphersuiteinfo-function"></a>SslLookupCipherSuiteInfo-Funktion

Die **SslLookupCipherSuiteInfo-Funktion** ruft die Verschlüsselungssammlungsinformationen für ein angegebenes Protokoll, eine Verschlüsselungssammlung und einen Schlüsseltypsatz ab.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslLookupCipherSuiteInfo(
  _In_  NCRYPT_PROV_HANDLE      hSslProvider,
  _In_  DWORD                   dwProtocol,
  _In_  DWORD                   dwCipherSuite,
  _In_  DWORD                   dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_SUITE *pCipherSuite,
  _In_  DWORD                   dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle für die [*SECURE SOCKETS LAYER Protokollanbieterinstanz*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*dwProtocol* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Protocol Identifier-Werte.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Cipher Suite Identifiers-Werte.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*dwKeyType* \[ In\]
</dt> <dd>

Einer der [**CNG SSL Provider Key Type Identifiers-Werte.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx)

</dd> <dt>

*pCipherSuite* \[ out\]
</dt> <dd>

Die Adresse eines Puffers, der eine [**NCRYPT \_ SSL \_ CIPHER \_ SUITE-Struktur**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) enthält, in die die Verschlüsselungssammlungsinformationen geschrieben werden.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, gibt sie einen Fehlerwert ungleich 0 (null) zurück.

Mögliche Rückgabecodes sind u. a. folgende:



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl> | Das *hSslProvider-Handle* ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

