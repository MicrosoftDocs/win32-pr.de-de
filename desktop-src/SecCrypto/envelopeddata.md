---
description: Das EnvelopedData-Objekt stellt Eigenschaften und Methoden bereit, um Daten mithilfe der Verschlüsselung für den Datenschutz zu umhüllen.
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
ms.openlocfilehash: e5309061c6ab315a089a1e1d8b9488556cae9f31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364910"
---
# <a name="envelopeddata-object"></a>EnvelopedData-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Das **EnvelopedData** -Objekt stellt Eigenschaften und Methoden bereit, um Daten mithilfe der Verschlüsselung für den Datenschutz zu umhüllen. Zum Umhüllen von Daten wird ein Sitzungs kryptografischer Schlüssel generiert. Dieser [*Sitzungsschlüssel*](../secgloss/s-gly.md) wird dann für jeden vorgesehenen Empfänger mit dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) des Zertifikats des Empfängers verschlüsselt. Die verschlüsselten Daten und der Satz Verschlüsselter Sitzungsschlüssel können an alle gewünschten Empfänger gesendet werden. Die generierte Nachricht weist das PKCS \# 7-Format auf.

## <a name="members"></a>Member

Das **EnvelopedData** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **EnvelopedData** -Objekt verfügt über diese Methoden.



| Methode                                   | BESCHREIBUNG                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Entschlüsseln**](envelopeddata-decrypt.md) | Entschlüsselt den eingeschlossenen Inhalt.<br/>                                                                      |
| [**Verschlüsseln**](envelopeddata-encrypt.md) | Verschlüsselt den Inhalt, verschlüsselt einen Sitzungsschlüssel für jeden Empfänger und gibt das verschlüsselte BLOB zurück.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **EnvelopedData** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                  | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithmus**](envelopeddata-algorithm.md)<br/>   | Lesen/Schreiben<br/> | Verschlüsselungsalgorithmus und [*Schlüssellänge*](../secgloss/k-gly.md).<br/>                                                                                                                                                                                                                                                                                                                              |
| [**Inhalt**](envelopeddata-content.md)<br/>       | Lesen/Schreiben<br/> | Der Klartext-Inhalt einer zu umzurufenden Nachricht. Das Festlegen dieser Eigenschaft muss erfolgen, bevor die [**Verschlüsselungs**](envelopeddata-encrypt.md) Methode aufgerufen wird.<br/> Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt, und alle verschlüsselten Inhalte im Objekt gehen verloren.<br/> Dies ist die Standard Eigenschaft.<br/> |
| [**Empfänger**](envelopeddata-recipients.md)<br/> | Schreibgeschützt<br/>  | Sammlung von [**Zertifikat**](certificate.md) Objekten, die die eingehüllte Nachricht empfangen.<br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Bemerkungen

Das **EnvelopedData** -Objekt kann erstellt und ist für die Skripterstellung sicher. Die ProgID für das **EnvelopedData** -Objekt ist CAPICOM. EnvelopedData. 1.

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

 

 
