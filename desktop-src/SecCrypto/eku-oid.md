---
description: Legt eine Zeichenfolge fest, die einen in Wincrypt.h definierten EKU-OID-Zeichenfolgenwert enthält, oder ruft sie ab.
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: IEKU::OID-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 49a35cb223c338573ba0a52288a1e5528820dcbd4c7589548ce31f9df46dc1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875250"
---
# <a name="iekuoid-property"></a>IEKU::OID-Eigenschaft

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **OID-Eigenschaft** legt eine Zeichenfolge fest, die einen in Wincrypt.h definierten EKU-OID-Zeichenfolgenwert enthält, oder ruft sie ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
EKU.OID As String
```



## <a name="property-value"></a>Eigenschaftswert

Zeichenfolge, die den in Wincrypt.h definierten EKU-OID-Zeichenfolgenwert enthält.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft verwendet nicht das [**in CAPICOM**](oid.md) 2.0 eingeführte OID-Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
