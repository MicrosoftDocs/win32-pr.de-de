---
description: Das PublicKey-Objekt stellt einen öffentlichen Schlüssel in einem Zertifikat Objekt dar.
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
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352149"
---
# <a name="publickey-object"></a>PublicKey-Objekt

\[Das **PublicKey** -Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2. PublicKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **PublicKey** -Objekt stellt einen öffentlichen Schlüssel in einem [**Zertifikat**](certificate.md) Objekt dar.

## <a name="when-to-use"></a>Verwendung

Das **PublicKey** -Objekt wird verwendet, um Daten zum öffentlichen Schlüssel abzurufen.

## <a name="members"></a>Member

Das **PublicKey** -Objekt verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **PublicKey** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp          | BESCHREIBUNG                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithmus**](publickey-algorithm.md)<br/>                 | Schreibgeschützt<br/> | Ruft das [**OID**](oid.md) -Objekt ab, das den vom öffentlichen Schlüssel verwendeten Algorithmus identifiziert. Dies ist die Standard Eigenschaft.<br/> |
| [**Encodkey**](publickey-encodedkey.md)<br/>               | Schreibgeschützt<br/> | Ruft ein [**encoddata**](encodeddata.md) -Objekt ab, das Zugriff auf den Wert des öffentlichen Schlüssels bereitstellt.<br/>                 |
| [**EncodedParameters**](publickey-encodedparameters.md)<br/> | Schreibgeschützt<br/> | Ruft ein [**encodeddata**](encodeddata.md) -Objekt ab, das Zugriff auf die Parameter des Algorithmus des öffentlichen Schlüssels bereitstellt.<br/>  |
| [**Länge**](publickey-length.md)<br/>                       | Schreibgeschützt<br/> | Ruft die Länge des öffentlichen Schlüssels in Bits ab.<br/>                                                                             |



 

## <a name="remarks"></a>Bemerkungen

Das **PublicKey** -Objekt kann nicht erstellt werden.

Das **PublicKey** -Objekt wird von der [**Certificate. PublicKey**](certificate-publickey.md) -Methode verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
