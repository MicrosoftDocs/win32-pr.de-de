---
description: Stellt Eigenschaften und Methoden zum Verschlüsseln und Entschlüsseln von Daten mit einem Sitzungsschlüssel bereit, der von einem geheimen Schlüssel abgeleitet ist.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: Verschlüsselteddata-Objekt
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
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364442"
---
# <a name="encrypteddata-object"></a>Verschlüsselteddata-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen den Platform invoationdienst (PInvoke), um die Win32-API-Funktionen [**cryptencryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) und [**cryptdecryptmessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) aufzurufen, um Nachrichten zu verschlüsseln und zu entschlüsseln. Weitere Informationen zu PInvoke finden Sie unter [Tutorial zum Platt Form Aufruf](https://msdn.microsoft.com/library/aa288468.aspx). Die [.net-und CryptoAPI über p/aufrufen: Teil 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) und [.net und CryptoAPI über p/aufrufen: Teil 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) Unterabschnitte der [Erweiterung von .net-Kryptografie mit CAPICOM und p/aufrufen](/previous-versions/ms867087(v=msdn.10)) können ebenfalls hilfreich sein.\]

Das **verschlüsselteddata** -Objekt stellt Eigenschaften und Methoden zum Verschlüsseln und Entschlüsseln von Daten mit einem [*Sitzungsschlüssel*](../secgloss/s-gly.md) bereit, der von einem geheimen Schlüssel abgeleitet ist.

> [!Note]  
> CAPICOM unterstützt den PKCS \# 7-Inhaltstyp "verschlüsselteddata" nicht, sondern verwendet eine nicht dem Standard entsprechende ASN-Struktur für " **verschlüsselteddata**". Daher kann nur CAPICOM ein CAPICOM-Objekt " **verschlüsselteddata** " entschlüsseln.

 

## <a name="members"></a>Member

Das **verschlüsselteddata** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **verschlüsselteddata** -Objekt verfügt über diese Methoden.



| Methode                                       | BESCHREIBUNG                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Entschlüsseln**](encrypteddata-decrypt.md)     | Entschlüsselt verschlüsselte Inhalte mit dem geheimen Schlüssel.<br/>                                 |
| [**Verschlüsseln**](encrypteddata-encrypt.md)     | Verschlüsselt den Inhalt mit dem aktuellen geheimen Schlüssel und Verschlüsselungsalgorithmus.<br/>      |
| [**Setsecret**](encrypteddata-setsecret.md) | Legt den geheimen Schlüssel fest, von dem der Verschlüsselungs-/Entschlüsselungs Sitzungsschlüssel abgeleitet wird.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **verschlüsselteddata** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithmus**](encrypteddata-algorithm.md)<br/> | Schreibgeschützt<br/>  | Der Algorithmus, der für die Verschlüsselung/Entschlüsselung verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Inhalt**](encrypteddata-content.md)<br/>     | Lesen/Schreiben<br/> | Der Inhalt, der verschlüsselt oder entschlüsselt werden soll. Das Festlegen dieser Eigenschaft muss erfolgen, bevor die [**Verschlüsselungs**](encrypteddata-encrypt.md) Methode aufgerufen wird. <br/> Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt, und alle verschlüsselten Inhalte im Objekt gehen verloren.<br/> Dies ist die Standard Eigenschaft.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Objekt " **verschlüsselteddata** " kann erstellt werden und ist für die Skripterstellung sicher. Die ProgID für das " **verschlüsselteddata** "-Objekt ist "CAPICOM". "Verschlüsselteddata. 1".

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
</dt> </dl>

 

 
