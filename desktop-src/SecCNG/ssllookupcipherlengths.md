---
description: Gibt eine NCrypt \_ \_ -SSL-Chiffre \_ Längen Struktur zurück, die die Header-und nach Spann Längen des Eingabe Protokolls, der Verschlüsselungs Sammlung und des Schlüssel Typs enthält.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: Ssllookupcipherlängen-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959381"
---
# <a name="ssllookupcipherlengths-function"></a>Ssllookupcipherlängen-Funktion

Die **ssllookupcipherlängen** -Funktion gibt eine [**NCrypt- \_ SSL- \_ Chiffre \_ Längen**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) Struktur zurück, die die Header-und nach Spann Längen des Eingabe Protokolls, der Verschlüsselungs Sammlung und des Schlüssel Typs enthält.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*dwprotocol* \[ in\]
</dt> <dd>

Einer der [**CNG-SSL-Anbieter Protokoll-Bezeichnerwerte**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwciphersuite* \[ in\]
</dt> <dd>

Einer der [**Cipher Suite-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwkeytype* \[ in\]
</dt> <dd>

Einer der [**Schlüsseltyp-Bezeichnerwerte des CNG-SSL-Anbieters**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) . Legen Sie für Schlüsseltypen, bei denen es sich nicht um eine [*Kryptographie*](/windows/desktop/SecGloss/e-gly) (ECC) handelt, diesen Parameter auf 0 (null) fest.

</dd> <dt>

*pcipherlängen* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der die [**NCrypt- \_ SSL- \_ Chiffre \_ Längen**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) Struktur empfängt.

</dd> <dt>

*cbcipherlängen* \[ in\]
</dt> <dd>

Die Länge des Puffers in Byte, auf den durch den *pcipherlength* -Parameter verwiesen wird.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Der *hsslprovider* -Parameter enthält einen ungültigen Zeiger.<br/>                                                      |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der *pcipherlength* -Parameter ist auf **null** festgelegt, oder die von *cbcipherlength* angegebene Pufferlänge ist zu kurz.<br/> |
| <dl> <dt>**Ernte \_ Ungültige \_ Flags**</dt> <dt>0x80090009l</dt> </dl>         | Der *dwFlags* -Parameter muss auf 0 (null) festgelegt werden.<br/>                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Die **ssllookupcipherlängen** -Funktion wird für die Konversationen von [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1,1 oder höher aufgerufen, um die Header-und nach Spann Längen für das angeforderte Protokoll, die Verschlüsselungs Sammlung und den Schlüsseltyp abzufragen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

