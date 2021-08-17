---
description: Ruft die Anzahl der PolicyInformation-Objekte in der Auflistung ab.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: CertificatePolicies.Count(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 405fbc928f6ff553abe3cd55d3f6e08a1aed13ef46093f912b6b08af45ec2c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771048"
---
# <a name="certificatepoliciescount-property"></a>CertificatePolicies.Count(Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates,**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) indem Sie den Konstruktor aufrufen, der eine OID als Parameter akzeptiert, und dann die OID für Zertifikatrichtlinien verwenden, um die Zertifikatrichtlinien abzurufen.\]

Die **Count-Eigenschaft** ruft die Anzahl der [**PolicyInformation-Objekte**](policyinformation.md) in der Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der [**PolicyInformation-Objekte**](policyinformation.md) in der Auflistung. Jedes **PolicyInformation-Objekt** stellt eine einzelne Zertifikatrichtlinie in der Auflistung dar.

## <a name="remarks"></a>Hinweise

Die **Count-Eigenschaft** kann verwendet werden, um das letzte [**PolicyInformation-Objekt**](policyinformation.md) in der Auflistung anzugeben, wenn ein bestimmtes **PolicyInformation-Objekt** mithilfe der [**CertificatePolicies.Item-Eigenschaft abgerufen**](certificatepolicies-item.md) wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
