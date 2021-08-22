---
description: Die OID-Eigenschaft ruft den Objektbezeichner für die Erweiterung ab. Dies ist die Standardeigenschaft.
ms.assetid: 51efd413-f9f0-4577-a554-de6afc32dd87
title: Extension.OID-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0cba2029884af965ca473f54948c20fee383fa9c22b3716c0fec0168e3e615f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006898"
---
# <a name="extensionoid-property"></a>Extension.OID-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **OID-Eigenschaft** ruft den Objektbezeichner für die Erweiterung ab. Dies ist die Standardeigenschaft.

## <a name="syntax"></a>Syntax


```VB
Extension.OID As OID
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**OID-Objekt,**](oid.md) das den Objektbezeichner der Erweiterung darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
