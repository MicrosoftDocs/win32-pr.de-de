---
description: Legt den Wert des Geheimnisses fest, der zum Ableiten des kryptografiesitzungsschlüssels verwendet wird, der zum Verschlüsseln und Entschlüsseln von Daten verwendet wird.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: Verschlüsselteddata. setsecret-Methode
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
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352847"
---
# <a name="encrypteddatasetsecret-method"></a>Verschlüsselteddata. setsecret-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktionen [**cryptencryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) aufzurufen, um Nachrichten zu verschlüsseln und zu entschlüsseln. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Die **setsecret** -Methode legt den Wert des Geheimnisses fest, der zum Ableiten des [*kryptografiesitzungsschlüssels*](../secgloss/s-gly.md) verwendet wird, der zum Verschlüsseln und Entschlüsseln von Daten verwendet wird.

## <a name="syntax"></a>Syntax


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die ein Geheimnis enthält, das zum Erstellen eines Sitzungs Kryptografieschlüssels verwendet wurde.

</dd> <dt>

*Secrettype* \[ in, optional\]
</dt> <dd>

Ein Wert der [**CAPICOM \_ Secret \_ Type**](capicom-secret-type.md) -Enumeration, die die Art des Geheimnisses angibt, das zum Generieren des Sitzungsschlüssels verwendet wurde. Der Standardwert ist CAPICOM \_ Secret \_ Password. Dieser Parameter kann den folgenden Wert aufweisen:



| Wert                                                                                                                                                                                        | Bedeutung                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**geheimer CAPICOM- \_ \_ Kennwort**</dt> </dl> | Der Verschlüsselungsschlüssel muss von einem Kennwort abgeleitet werden.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der geheime Schlüssel wird zum Erstellen des Sitzungsschlüssels für die Verschlüsselung oder Entschlüsselung verwendet. Für beide Vorgänge muss das gleiche Geheimnis verwendet werden. Wenn der geheime Schlüssel für die Datenverschlüsselung verloren geht, können die verschlüsselten Daten nicht entschlüsselt werden.

Verwenden Sie ggf. " [**cryptprotectmemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) " oder " [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) ", um den geheimen Schlüssel vor und nach der Verwendung zu schützen. Löschen Sie den Arbeitsspeicher, der dem geheimen Schlüssel zugeordnet ist

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

 

 
