---
description: Richtet den Signatur Geber eines SignedData-oder signedcode-Objekts ein.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Signatur Geber Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372696"
---
# <a name="signer-object"></a>Signatur Geber Objekt

\[Das **Signatur** Geber Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Das **Signatur** Geber Objekt richtet den Signatur Geber eines [**SignedData**](signeddata.md) -oder [**signedcode**](signedcode.md) -Objekts ein. Das [**Zertifikat**](certificate.md) des **Signatur** Geber Objekts muss über einen verfügbaren privaten Schlüssel verfügen, der zum Signieren von Daten verwendet werden kann.

## <a name="members"></a>Member

Das **Signatur** Geber Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Signatur** Geber Objekt verfügt über diese Methoden.



| Methode                      | BESCHREIBUNG                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [**Laden**](signer-load.md) | Lädt ein Signaturzertifikat aus einer angegebenen PFX-Datei.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Signatur** Geber Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                     | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Authenticatedattributes**](signer-authenticatedattributes.md)<br/> | Schreibgeschützt<br/>  | Die Auflistung von authentifizierten Attributen.<br/>                                                                                                                                                                                                                                                                                      |
| [**Stellt**](signer-certificate.md)<br/>                         | Lesen/Schreiben<br/> | Das [**Zertifikat**](certificate.md) Objekt, das das Zertifikat eines Signatur Gebers der Daten darstellt.<br/> Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt.<br/> Dies ist die Standard Eigenschaft.<br/> |
| [**Ketten**](signer-chain.md)<br/>                                     | Schreibgeschützt<br/>  | Die Kette des Signatur Gebers.<br/>                                                                                                                                                                                                                                                                                                         |
| [**Optionen**](signer-options.md)<br/>                                 | Lesen/Schreiben<br/> | Legt die Zertifikat Option des Signatur Gebers fest oder ruft Sie ab.<br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Bemerkungen

Das **Signatur** Geber Objekt kann erstellt werden und ist für die Skripterstellung sicher. Die ProgID für das **Signatur** Geber Objekt ist CAPICOM. Signatur Geber. 2.

**CAPICOM 1. *x*:** die ProgID für das **Signatur** Geber Objekt ist CAPICOM. Signer. 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
