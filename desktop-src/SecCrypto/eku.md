---
description: Stellt eine einzelne EKU-Eigenschaft (Extended Key Usage) eines Zertifikats dar.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: EKU-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bd887204abc31583e596e94c25b64addcfe8109e6432845d25d939fd8e79e2d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875140"
---
# <a name="eku-object"></a>EKU-Objekt

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System.Security.Cryptography.X509Certificates-Namespace.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Das **EKU-Objekt** stellt eine einzelne EKU-Eigenschaft (Extended Key Usage) eines Zertifikats dar.

## <a name="members"></a>Member

Das **EKU-Objekt** weist diese Typen von Membern auf:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **EKU-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Name**](eku-name.md)<br/> | Lesen/Schreiben<br/> | Legt einen Enumerationswert fest, der den CAPICOM-Namen der EKU angibt, oder ruft diesen ab. Dies ist die Standardeigenschaft.<br/>                                                                                   |
| [**Oid**](eku-oid.md)<br/>   | Lesen/Schreiben<br/> | Legt eine Zeichenfolge fest, die einen in Wincrypt.h definierten [*EKU-Objektbezeichner -Zeichenfolgenwert*](../secgloss/o-gly.md) (OID) enthält, oder ruft sie ab.<br/> |



 

## <a name="remarks"></a>Hinweise

Das **EKU-Objekt** wird von der folgenden Auflistung und Eigenschaft verwendet:

-   [**EKUs-Sammlung**](ekus.md)
-   [**CertificateStatus.EKU-Eigenschaft**](certificatestatus-eku.md)

Das **EKU-Objekt** kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
