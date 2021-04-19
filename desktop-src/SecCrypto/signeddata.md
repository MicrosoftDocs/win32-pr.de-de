---
description: Stellt Eigenschaften und Methoden bereit, um den Inhalt zu erstellen, der mit einer digitalen Signatur signiert werden soll, um Daten digital zu signieren oder cosignieren, und um die digitale Signatur der signierten Daten zu überprüfen. Die signierte Nachricht weist das PKCS \# 7-Format auf.
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: SignedData-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360305"
---
# <a name="signeddata-object"></a>SignedData-Objekt

\[Das **SignedData** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Das **SignedData** -Objekt stellt Eigenschaften und Methoden bereit, um den Inhalt zu erstellen, der mit einer [*digitalen Signatur*](../secgloss/d-gly.md)signiert werden soll, um Daten digital zu signieren oder cosignieren, und um die digitale Signatur der signierten Daten zu überprüfen. Die signierte Nachricht weist das PKCS \# 7-Format auf.

Wenn eine Daten Signatur überprüft wird, wird die Zuordnung zwischen einem Signatur Geber und Daten bestätigt, und es wird angezeigt, dass die Daten nach der Erstellung der Signatur nicht geändert wurden.

## <a name="members"></a>Member

Das **SignedData** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SignedData** -Objekt verfügt über diese Methoden.



| Methode                              | BESCHREIBUNG                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [**Cosign**](signeddata-cosign.md) | Signiert eine bereits signierte Nachricht mit einem Vorzeichen.<br/>                       |
| [**Gebärden**](signeddata-sign.md)     | Erstellt eine digitale Signatur für den zu Signier enden Inhalt.<br/> |
| [**Weisen**](signeddata-verify.md) | Bestimmt die Gültigkeit einer Signatur oder von Signaturen.<br/>    |



 

### <a name="properties"></a>Eigenschaften

Das **SignedData** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zertifikate**](signeddata-certificates.md)<br/> | Schreibgeschützt<br/>  | Ruft die [**Zertifikats**](certificates.md) Sammlung der signierten Daten ab.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**Inhalt**](signeddata-content.md)<br/>           | Lesen/Schreiben<br/> | Zu Signier Ende Daten. Diese Eigenschaft muss initialisiert werden, bevor die [**Sign**](signeddata-sign.md) -Methode aufgerufen wird.<br/> Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt, und alle Signaturen, die dem-Objekt zugeordnet waren, bevor die-Eigenschaft geändert wurde, gehen verloren.<br/> Dies ist die Standard Eigenschaft.<br/> |
| [**Signatur Geber**](signeddata-signers.md)<br/>           | Schreibgeschützt<br/>  | Ruft die Signatur Geber Auflistung ab [**, die die**](signers.md) Signatur Ersteller der Daten darstellt.<br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Das **SignedData** -Objekt kann erstellt und ist für die Skripterstellung sicher. Die ProgID für das **SignedData** -Objekt ist CAPICOM. SignedData. 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
