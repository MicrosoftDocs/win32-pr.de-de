---
description: Ruft die Anzahl der Certificate-Objekte in der Auflistung ab.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Certificates.Count (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 703b929ee4b9cbe69a0f2ff37ad7e1d0c2c0005c0aa461fc38a14baa8a8ab443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770549"
---
# <a name="certificatescount-property"></a>Certificates.Count (Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Count-Eigenschaft** ruft die Anzahl der [**Certificate-Objekte**](certificate.md) in der Auflistung ab.

## <a name="syntax"></a>Syntax


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der [**Zertifikatobjekte**](certificate.md) in der Auflistung. Jedes **Certificate-Objekt** stellt ein einzelnes Zertifikat in der Auflistung dar.

## <a name="remarks"></a>Hinweise

CAPICOM unterstützt nur ein einzelnes Zertifikat für den [*Smartcardspeicher.*](../secgloss/s-gly.md) Auch wenn der Smartcardspeicher mehr als ein Zertifikat enthält, enthält diese Eigenschaft 1. Weitere Informationen zum Smartcardspeicher finden Sie im **CAPICOM \_ SMART CARD USER \_ \_ \_ STORE-Member** der [**CAPICOM \_ STORE \_ LOCATION-Enumeration.**](capicom-store-location.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Zertifikate**](certificates.md)
</dt> </dl>

 

 
