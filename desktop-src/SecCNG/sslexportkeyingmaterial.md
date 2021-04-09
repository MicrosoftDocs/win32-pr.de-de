---
description: Exportiert das Schlüsselmaterial gemäß RFC 5705-Standard.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Sslexportkeyingmaterial-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760105"
---
# <a name="sslexportkeyingmaterial-function"></a>Sslexportkeyingmaterial-Funktion

Exportiert das Schlüsselmaterial gemäß [RFC 5705-Standard](https://tools.ietf.org/html/rfc5705). Diese Funktion verwendet die Funktion "TLS Pseudo Zufalls", um einen Byte Puffer mit Schlüsselmaterial zu erhalten. Es wird ein Verweis auf den geheimen Hauptschlüssel, die Mehrdeutigkeit der ASCII-Bezeichnung, Client-und Server Zufallswerte und optional die Anwendungskontext Daten benötigt.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der TLS-Protokoll Anbieter Instanz.

</dd> <dt>

*hmasterkey* \[ in\]
</dt> <dd>

Das Handle des Hauptschlüssel Objekts, das verwendet wird, um das Schlüsselmaterial zu erstellen, das von BR exportiert wird.

</dd> <dt>

*slabel* \[ in\]
</dt> <dd>

eine Zeichenfolge mit einer Zeichenfolge, die eine Zeichenfolge mit Zeichen SChannel entfernt das abschließende NUL-Zeichen, bevor es an die Pseudo Zufalls-Funktion übergeben wird.

</dd> <dt>

*pbrandoms* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine Verkettung der *\_ zufälligen* Zufallswerte des *Clients \_* und des Servers der TLS-Verbindung enthält.

</dd> <dt>

*cbrandoms* \[ in\]
</dt> <dd>

Die Länge des *pbrandoms* -Puffers in Bytes.

</dd> <dt>

*pbcontextvalue* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Anwendungskontext enthält. Wenn *pbcontextvalue* **null** ist, muss *cbcontextvalue* gleich NULL sein.

</dd> <dt>

*cbcontextvalue* \[ in\]
</dt> <dd>

Die Länge des *pbcontextvalue* -Puffers in Bytes.

</dd> <dt>

*pboutput* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Puffers, der das exportierte Schlüsselmaterial empfängt. Der *cboutput* -Parameter enthält die Größe dieses Puffers. Dieser Wert darf nicht **null** sein.

</dd> <dt>

*cboutput* \[ in\]
</dt> <dd>

Die Länge des *pboutput* -Puffers in Bytes. Muss größer sein als Null.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Nicht verwendet. Muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl> | Eines der bereitgestellten Handles ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




