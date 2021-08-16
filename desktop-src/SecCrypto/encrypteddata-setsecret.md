---
description: Legt den Wert des Geheimnisses fest, das zum Ableiten des kryptografischen Sitzungsschlüssels verwendet wird, der zum Verschlüsseln und Entschlüsseln von Daten verwendet wird.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: EncryptedData.SetSecret-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0e56bd490c4e665d900eb39fb57d09019ab4cfa3b1eb3ad06ad74cb4e83514ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766445"
---
# <a name="encrypteddatasetsecret-method"></a>EncryptedData.SetSecret-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen Platform Invocation Services (PInvoke) zum Aufrufen der Win32-API-Funktionen [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**CryptDecryptMessage,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) um Nachrichten zu verschlüsseln und zu entschlüsseln. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) .NET und CryptoAPI über [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Teil 1 und .NET und [CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Unterabschnitte [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) (Erweitern der .NET-Kryptografie mit CAPICOM und P/Invoke) können ebenfalls hilfreich sein.\]

Die **SetSecret-Methode** legt den Wert des Geheimnisses fest, das zum Ableiten des kryptografischen Sitzungsschlüssels verwendet wird, der zum Verschlüsseln und Entschlüsseln von Daten verwendet wird. [](../secgloss/s-gly.md)

## <a name="syntax"></a>Syntax


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die ein Geheimnis enthält, das zum Erstellen eines kryptografischen Sitzungsschlüssels verwendet wird.

</dd> <dt>

*SecretType* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ SECRET \_ TYPE-Enumeration,**](capicom-secret-type.md) der die Art des Geheimnisses angibt, das zum Generieren des Sitzungsschlüssels verwendet wird. Der Standardwert ist CAPICOM \_ SECRET \_ PASSWORD. Dieser Parameter kann der folgende Wert sein.



| Wert                                                                                                                                                                                        | Bedeutung                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**CAPICOM \_ SECRET \_ PASSWORD**</dt> </dl> | Der Verschlüsselungsschlüssel muss von einem Kennwort abgeleitet werden.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Geheimnis wird verwendet, um den Sitzungsschlüssel für die Verschlüsselung oder Entschlüsselung zu erstellen. Für beide Vorgänge muss dasselbe Geheimnis verwendet werden. Wenn das Geheimnis, das zum Verschlüsseln von Daten verwendet wird, verloren geht, können die verschlüsselten Daten nicht entschlüsselt werden.

Wenn dies für Ihre Anwendung geeignet ist, sollten Sie [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) oder [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) verwenden, um das Geheimnis vor und nach der Verwendung zu schützen. Löschen Sie den Speicher, der dem Geheimnis zugeordnet ist, wenn Sie fertig sind.

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

 

 
