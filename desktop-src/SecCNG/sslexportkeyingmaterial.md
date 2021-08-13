---
description: Exportiert Schlüsselmaterial gemäß RFC 5705-Standard.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: SslExportKeyingMaterial-Funktion (Sslprovider.h)
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
ms.openlocfilehash: 39aaebba64f92794e179af95a5a175e2603fccc40410989cfcd427c6a7a1a88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906618"
---
# <a name="sslexportkeyingmaterial-function"></a>SslExportKeyingMaterial-Funktion

Exportiert Schlüsselmaterial gemäß [RFC 5705-Standard.](https://tools.ietf.org/html/rfc5705) Diese Funktion verwendet die TLS-Pseudozufallsfunktion, um einen Bytepuffer mit Schlüsselmaterial zu erzeugen. Sie verwendet einen Verweis auf den geheimen Hauptschlüssel, die eindeutigen ASCII-Bezeichnungen, zufälligen Client- und Serverwerte und optional die Anwendungskontextdaten.

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

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der TLS-Protokollanbieterinstanz.

</dd> <dt>

*hMasterKey* \[ In\]
</dt> <dd>

Das Handle des Hauptschlüsselobjekts, das zum Erstellen des zu exportierenden Schlüsselmaterials verwendet wird.

</dd> <dt>

*sLabel* \[ In\]
</dt> <dd>

eine AUF NUL endende ASCII-Bezeichnungszeichenfolge. Schannel entfernt das abschließende NUL-Zeichen, bevor es an die Pseudozufallsfunktion übergeben wird.

</dd> <dt>

*pbRandoms* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine Verkettung der *\_ zufälligen Client-* und *\_ Serverzufallswerte* der TLS-Verbindung enthält.

</dd> <dt>

*cbRandoms* \[ In\]
</dt> <dd>

Die Länge des *pbRandoms-Puffers* in Bytes.

</dd> <dt>

*pbContextValue* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Anwendungskontext enthält. Wenn *pbContextValue* **NULL** ist, muss *cbContextValue* 0 (null) sein.

</dd> <dt>

*cbContextValue* \[ In\]
</dt> <dd>

Die Länge des *pbContextValue-Puffers* in Bytes.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Die Adresse eines Puffers, der das exportierte Schlüsselmaterial empfängt. Der *cbOutput-Parameter* enthält die Größe dieses Puffers. Dieser Wert darf nicht **NULL** sein.

</dd> <dt>

*cbOutput* \[ In\]
</dt> <dd>

Die Länge des *pbOutput-Puffers* in Bytes. Muss größer sein als Null.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Wird nicht verwendet. Muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl> | Einer der bereitgestellten Handles ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




