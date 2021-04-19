---
description: Entschlüsselt eine verschlüsselte und codierte Daten Zeichenfolge.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: Verschlüsselteddata. entschlpt-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aa702a5cefc46f6d0cbe5d7e0fba17ff03596b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370558"
---
# <a name="encrypteddatadecrypt-method"></a>Verschlüsselteddata. entschlpt-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktionen [**cryptencryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) aufzurufen, um Nachrichten zu verschlüsseln und zu entschlüsseln. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **Entschlüsselungsmethode** entschlüsselt eine verschlüsselte und codierte Daten Zeichenfolge. Die sich daraus ergebenden Klartext-Daten werden zur [**Content**](encrypteddata-content.md) -Eigenschaft des [**verschlüsselteddata**](encrypteddata.md) -Objekts. Das Entschlüsseln des Inhalts schlägt fehl, es sei denn, der geheime Schlüssel, der von der [**setsecret**](encrypteddata-setsecret.md) -Methode festgelegt wird, ist identisch mit dem geheimen Schlüssel, der zum Ableiten des Schlüssels verwendet wurde

## <a name="syntax"></a>Syntax


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Verschlüsseltedmessage* \[ " in\]
</dt> <dd>

Eine Zeichenfolge, die die verschlüsselten, verschlüsselten Daten enthält, die entschlüsselt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der vom aktuellen geheimen Schlüssel abgeleitete Sitzungsschlüssel wird für die Entschlüsselung verwendet. Diese Methode erzeugt nicht den richtigen Klartext, es sei denn, das aktuelle Geheimnis stimmt genau mit dem geheimen Schlüssel überein, der zum Verschlüsseln der Nachricht verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
