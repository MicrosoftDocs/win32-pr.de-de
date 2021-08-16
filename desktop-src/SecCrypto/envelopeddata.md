---
description: Das EnvelopedData-Objekt stellt Eigenschaften und Methoden zum Umhen von Daten für den Datenschutz durch Verschlüsselung zur Kenntnis.
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: EnvelopedData-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: af88fd9b4be0c7ddd9fe5dfc204558c1a36cab418166f73c8de0ec0c06c0a8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766111"
---
# <a name="envelopeddata-object"></a>EnvelopedData-Objekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**Namespace System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Das **EnvelopedData-Objekt** stellt Eigenschaften und Methoden zum Umhen von Daten für den Datenschutz durch Verschlüsselung zur Kenntnis. Zum Umhing von Daten wird ein kryptografischer Sitzungsschlüssel generiert. Dieser [*Sitzungsschlüssel*](../secgloss/s-gly.md) wird dann für jeden [](../secgloss/p-gly.md) vorgesehenen Empfänger mit dem öffentlichen Schlüssel des Empfängers aus dem Zertifikat des Empfängers verschlüsselt. Die verschlüsselten Daten und der Satz verschlüsselter Sitzungsschlüssel können an alle vorgesehenen Empfänger gesendet werden. Die generierte Nachricht hat das PKCS \# 7-Format.

## <a name="members"></a>Member

Das **EnvelopedData-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **EnvelopedData-Objekt** verfügt über diese Methoden.



| Methode                                   | Beschreibung                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Entschlüsseln**](envelopeddata-decrypt.md) | Entschlüsselt umhumhierten Inhalt.<br/>                                                                      |
| [**Encrypt**](envelopeddata-encrypt.md) | Verschlüsselt den Inhalt, verschlüsselt einen Sitzungsschlüssel für jeden Empfänger und gibt das verschlüsselte BLOB zurück.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **EnvelopedData-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                  | Zugriffstyp           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithmus**](envelopeddata-algorithm.md)<br/>   | Lesen/Schreiben<br/> | Verschlüsselungsalgorithmus und [*Schlüssellänge*](../secgloss/k-gly.md).<br/>                                                                                                                                                                                                                                                                                                                              |
| [**Inhalt**](envelopeddata-content.md)<br/>       | Lesen/Schreiben<br/> | Der Klartextinhalt einer Umschlagnachricht. Das Festlegen dieser Eigenschaft muss vor dem Aufrufen der [**Encrypt-Methode**](envelopeddata-encrypt.md) erfolgen.<br/> Wenn der Wert dieser Eigenschaft direkt oder indirekt [](../secgloss/s-gly.md) zurückgesetzt wird, wird der gesamte Zustand des Objekts zurückgesetzt, und alle verschlüsselten Inhalte im Objekt gehen verloren.<br/> Dies ist die Standardeigenschaft.<br/> |
| [**Empfänger**](envelopeddata-recipients.md)<br/> | Schreibgeschützt<br/>  | Sammlung von [**Zertifikatobjekten,**](certificate.md) um die umhumschlagte Nachricht zu empfangen.<br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Hinweise

Das **EnvelopedData-Objekt** kann erstellt werden und ist sicher für Skripts. Die ProgID für das **EnvelopedData-Objekt** ist CAPICOM. EnvelopedData.1.

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
</dt> </dl>

 

 
