---
description: Ruft den Wert einer benannten Eigenschaft für ein SSL-Anbieter Schlüsselobjekt (Secure Sockets Layer Protocol) ab.
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Sslgetkeyproperty-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352259"
---
# <a name="sslgetkeyproperty-function"></a>Sslgetkeyproperty-Funktion

Die **sslgetkeyproperty** -Funktion Ruft den Wert einer benannten Eigenschaft für ein SSL-Anbieter Schlüsselobjekt ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) ab.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HKEY* \[ in\]
</dt> <dd>

Das Handle des SSL-Anbieters.

</dd> <dt>

*pszproperty* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Namen der abzurufenden Eigenschaft enthält. Hierbei kann es sich um einen der vordefinierten [**Schlüsselspeicher-Eigenschaften**](key-storage-property-identifiers.md) Bezeichner oder um einen benutzerdefinierten Eigenschaften Bezeichner handeln.

</dd> <dt>

*ppboutput* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Eigenschafts Wert empfängt. Der Aufrufer der Funktion muss diesen Puffer durch Aufrufen der [**sslfreebuffer**](sslfreebuffer.md) -Funktion freigeben.

</dd> <dt>

*pcboutput* \[ vorgenommen\]
</dt> <dd>

Die Größe des *pboutput* -Puffers in Bytes.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Eines der bereitgestellten Handles ist ungültig.<br/>    |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Einer der angegebenen Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

