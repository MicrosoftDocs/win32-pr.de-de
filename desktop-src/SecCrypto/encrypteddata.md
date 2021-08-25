---
description: Stellt Eigenschaften und Methoden zum Verschlüsseln und Entschlüsseln von Daten mithilfe eines sitzungsschlüssels zur Folge, der von einem Geheimnis abgeleitet ist.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: EncryptedData-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 15a66640ccdf794e88ae9cff04854a40fcfa6b763259da191bcdc6b07f11f449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874490"
---
# <a name="encrypteddata-object"></a>EncryptedData-Objekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen Platform Invocation Services (PInvoke) zum Aufrufen der Win32-API-Funktionen [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**CryptDecryptMessage,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) um Nachrichten zu verschlüsseln und zu entschlüsseln. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zu Plattformaufrufen.](https://msdn.microsoft.com/library/aa288468.aspx) .NET und CryptoAPI über [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Teil 1 und .NET und [CryptoAPI über P/Invoke: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) der Unterabschnitte [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) (Erweitern der .NET-Kryptografie mit CAPICOM und P/Invoke) können ebenfalls hilfreich sein.\]

Das **EncryptedData-Objekt** stellt Eigenschaften und Methoden zum Verschlüsseln und Entschlüsseln von Daten mithilfe eines Sitzungsschlüssels zur [*Anwendung, der*](../secgloss/s-gly.md) von einem Geheimnis abgeleitet wurde.

> [!Note]  
> CAPICOM unterstützt den PKCS 7 EncryptedData-Inhaltstyp nicht, verwendet jedoch eine nicht \# standardmäßige ASN-Struktur für **EncryptedData.** Daher kann nur CAPICOM ein CAPICOM **EncryptedData-Objekt** entschlüsseln.

 

## <a name="members"></a>Member

Das **EncryptedData-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **EncryptedData-Objekt** verfügt über diese Methoden.



| Methode                                       | BESCHREIBUNG                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Entschlüsseln**](encrypteddata-decrypt.md)     | Entschlüsselt verschlüsselte Inhalte mithilfe des Geheimnisses.<br/>                                 |
| [**Encrypt**](encrypteddata-encrypt.md)     | Verschlüsselt den Inhalt mit dem aktuellen Geheimnis und Verschlüsselungsalgorithmus.<br/>      |
| [**SetSecret**](encrypteddata-setsecret.md) | Legt das Geheimnis fest, von dem der Verschlüsselungs-/Entschlüsselungssitzungsschlüssel abgeleitet wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **EncryptedData-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithmus**](encrypteddata-algorithm.md)<br/> | Schreibgeschützt<br/>  | Algorithmus, der für die Verschlüsselung/Entschlüsselung verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Inhalt**](encrypteddata-content.md)<br/>     | Lesen/Schreiben<br/> | Der zu verschlüsselnde oder zu entschlüsselnde Inhalt. Das Festlegen dieser Eigenschaft muss vor dem Aufrufen der [**Encrypt-Methode**](encrypteddata-encrypt.md) erfolgen. <br/> Wenn der Wert dieser Eigenschaft direkt oder indirekt [](../secgloss/s-gly.md) zurückgesetzt wird, wird der gesamte Zustand des Objekts zurückgesetzt, und alle verschlüsselten Inhalte im Objekt gehen verloren.<br/> Dies ist die Standardeigenschaft.<br/> |



 

## <a name="remarks"></a>Hinweise

Das **EncryptedData-Objekt** kann erstellt werden und ist sicher für Skripts. Die ProgID für das **EncryptedData-Objekt** ist CAPICOM. EncryptedData.1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
