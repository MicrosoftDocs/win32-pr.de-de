---
description: Entschlüsselt eine verschlüsselte und codierte Datenzeichenfolge.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: EncryptedData.Decrypt-Methode
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
ms.openlocfilehash: 8bf8a108efdc462a9f08a508a05b736817ec38ce43ee50dbd3fdd11aa2af9f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766696"
---
# <a name="encrypteddatadecrypt-method"></a>EncryptedData.Decrypt-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen Platform Invocation Services (PInvoke) zum Aufrufen der Win32-API-Funktionen [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**CryptDecryptMessage,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) um Nachrichten zu verschlüsseln und zu entschlüsseln. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) .NET und CryptoAPI über [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Teil 1 und .NET und [CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Unterabschnitte [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) (Erweitern der .NET-Kryptografie mit CAPICOM und P/Invoke) können ebenfalls hilfreich sein.\]

Die **Decrypt-Methode** entschlüsselt eine verschlüsselte und codierte Datenzeichenfolge. Die resultierenden Klartextdaten werden zur [**Content-Eigenschaft**](encrypteddata-content.md) des [**EncryptedData-Objekts.**](encrypteddata.md) Die Entschlüsselung des Inhalts schlägt fehl, es sei denn, das geheimnis, das von der [**SetSecret-Methode**](encrypteddata-setsecret.md) festgelegt wird, ist genau dasselbe wie das Geheimnis, das zum Ableiten des Schlüssels verwendet wird, der zum Verschlüsseln des Inhalts verwendet wird.

## <a name="syntax"></a>Syntax


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EncryptedMessage* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die die codierten, verschlüsselten Daten enthält, die entschlüsselt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der vom aktuellen Geheimnis abgeleitete Sitzungsschlüssel wird für die Entschlüsselung verwendet. Diese Methode erzeugt nur dann den richtigen Klartext, wenn das aktuelle Geheimnis genau mit dem geheimen Schlüssel zum Verschlüsseln der Nachricht entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**Encrypteddata**](encrypteddata.md)
</dt> </dl>

 

 
