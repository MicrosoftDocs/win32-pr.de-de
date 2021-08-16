---
description: Richtet den Signaturgeber eines SignedData- oder SignedCode-Objekts ein.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Signer-Objekt
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
ms.openlocfilehash: 4da0f63c64a85290d5b36cad046446a9a0feedcd897869a0df1932ee2532a687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898512"
---
# <a name="signer-object"></a>Signer-Objekt

\[Das **Signer-Objekt** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Das **Signer-Objekt** richtet den Signaturgeber eines [**SignedData-**](signeddata.md) oder [**SignedCode-Objekts**](signedcode.md) ein. Das [**Zertifikat**](certificate.md) des **Signer-Objekts** muss über einen verfügbaren privaten Schlüssel verfügen, der zum Signieren von Daten verwendet werden kann.

## <a name="members"></a>Member

Das **Signer-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Signer-Objekt** verfügt über diese Methoden.



| Methode                      | BESCHREIBUNG                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [**Laden**](signer-load.md) | Lädt ein Signaturzertifikat aus einer angegebenen PFX-Datei.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **Signer-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                     | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticatedAttributes**](signer-authenticatedattributes.md)<br/> | Schreibgeschützt<br/>  | Die Auflistung authentifizierter Attribute.<br/>                                                                                                                                                                                                                                                                                      |
| [**Zertifikat**](signer-certificate.md)<br/>                         | Lesen/Schreiben<br/> | Das [**Certificate-Objekt,**](certificate.md) das das Zertifikat eines Signierers der Daten darstellt.<br/> Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Zustand*](../secgloss/s-gly.md) des Objekts zurückgesetzt.<br/> Dies ist die Standardeigenschaft.<br/> |
| [**Kette**](signer-chain.md)<br/>                                     | Schreibgeschützt<br/>  | Die Kette des Signierers.<br/>                                                                                                                                                                                                                                                                                                         |
| [**Optionen**](signer-options.md)<br/>                                 | Lesen/Schreiben<br/> | Legt die Zertifikatoption des Signierers fest oder ruft sie ab.<br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Hinweise

Das **Signer-Objekt** kann erstellt werden und ist für Skripts sicher. Die ProgID für das **Signer-Objekt** ist CAPICOM. Signer.2.

**CAPICOM 1. *x*:** Die ProgID für das **Signer-Objekt** ist CAPICOM. Signer.1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 
