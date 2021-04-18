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
ms.openlocfilehash: ff397ae747ecd09dd1292e5c15eb4291692d9651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365743"
---
# <a name="eku-object"></a>EKU-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **EKU** -Objekt stellt eine einzelne EKU (Extended Key Usage)-Eigenschaft eines Zertifikats dar.

## <a name="members"></a>Member

Das **EKU** -Objekt verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **EKU** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Name**](eku-name.md)<br/> | Lesen/Schreiben<br/> | Legt einen Enumerationswert fest, der den CAPICOM-Namen der EKU angibt, oder ruft ihn ab. Dies ist die Standard Eigenschaft.<br/>                                                                                   |
| [**OID**](eku-oid.md)<br/>   | Lesen/Schreiben<br/> | Legt eine Zeichenfolge fest oder ruft eine Zeichenfolge ab, die einen in Wincrypt. h definierten EKU- [*Objekt Bezeichner*](../secgloss/o-gly.md) (OID)-Zeichen folgen Wert enthält.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das **EKU** -Objekt wird von der folgenden Auflistung und Eigenschaft verwendet:

-   [**EKUs**](ekus.md) -Sammlung
-   [**CertificateStatus. EKU**](certificatestatus-eku.md) -Eigenschaft

Das **EKU** -Objekt kann nicht erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
