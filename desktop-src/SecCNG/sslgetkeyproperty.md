---
description: Ruft den Wert einer benannten Eigenschaft für ein SSL-Anbieterschlüsselobjekt (Secure Sockets Layer Protokoll) ab.
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: SslGetKeyProperty-Funktion (Sslprovider.h)
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
ms.openlocfilehash: b86f8a2e76573122bcfcf809d5301bc6bf70690467527f4dc69a5ec12419f56b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906118"
---
# <a name="sslgetkeyproperty-function"></a>SslGetKeyProperty-Funktion

Die **SslGetKeyProperty-Funktion** ruft den Wert einer benannten Eigenschaft für ein SSL-Schlüsselobjekt [*(Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) Protocol) ab.

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

*hKey* \[ In\]
</dt> <dd>

Das Handle des SSL-Anbieters.

</dd> <dt>

*pszProperty* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete Unicode-Zeichenfolge, die den Namen der abzurufenden Eigenschaft enthält. Dies kann einer der vordefinierten [**Schlüssel-Storage-Eigenschaftsbezeichner oder**](key-storage-property-identifiers.md) ein benutzerdefinierter Eigenschaftenbezeichner sein.

</dd> <dt>

*ppbOutput* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Eigenschaftswert empfängt. Der Aufrufer der Funktion muss diesen Puffer durch Aufrufen der [**SslFreeBuffer-Funktion frei**](sslfreebuffer.md) geben.

</dd> <dt>

*vor der Sperre* \[ out\]
</dt> <dd>

Die Größe des *pbOutput-Puffers in* Bytes.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, gibt sie einen Fehlerwert ungleich 0 (null) zurück.

Mögliche Rückgabecodes sind u. a. folgende:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Eines der bereitgestellten Handles ist ungültig.<br/>    |
| <dl> <dt>**NTE \_ UNGÜLTIGER \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Einer der angegebenen Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

