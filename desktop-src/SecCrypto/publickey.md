---
description: Das PublicKey-Objekt stellt einen öffentlichen Schlüssel in einem Certificate-Objekt dar.
title: PublicKey-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d27a89d51840e70563854b3cc7f9084b6bd42cb5707630755e771d610c64a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901347"
---
# <a name="publickey-object"></a>PublicKey-Objekt

\[Das **PublicKey-Objekt** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509Certificate2.PublicKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) im [**System.Security.Cryptography.X509Certificates-Namespace.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Das **PublicKey-Objekt** stellt einen öffentlichen Schlüssel in einem [**Certificate-Objekt**](certificate.md) dar.

## <a name="when-to-use"></a>Verwendung

Das **PublicKey-Objekt** wird verwendet, um Daten über den öffentlichen Schlüssel abzurufen.

## <a name="members"></a>Member

Das **PublicKey-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **PublicKey-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp          | Beschreibung                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithmus**](publickey-algorithm.md)<br/>                 | Schreibgeschützt<br/> | Ruft das [**OID-Objekt**](oid.md) ab, das den vom öffentlichen Schlüssel verwendeten Algorithmus identifiziert. Dies ist die Standardeigenschaft.<br/> |
| [**EncodedKey**](publickey-encodedkey.md)<br/>               | Schreibgeschützt<br/> | Ruft ein [**EncodedData-Objekt**](encodeddata.md) ab, das Zugriff auf den Wert des öffentlichen Schlüssels bereitstellt.<br/>                 |
| [**EncodedParameters**](publickey-encodedparameters.md)<br/> | Schreibgeschützt<br/> | Ruft ein [**EncodedData-Objekt**](encodeddata.md) ab, das Zugriff auf die Parameter des Algorithmus für öffentliche Schlüssel bereitstellt.<br/>  |
| [**Länge**](publickey-length.md)<br/>                       | Schreibgeschützt<br/> | Ruft die Länge des öffentlichen Schlüssels in Bits ab.<br/>                                                                             |



 

## <a name="remarks"></a>Hinweise

Das **PublicKey-Objekt** kann nicht erstellt werden.

Das **PublicKey-Objekt** wird von der [**Certificate.PublicKey-Methode**](certificate-publickey.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
