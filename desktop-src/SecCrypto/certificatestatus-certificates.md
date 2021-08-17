---
description: Legt die Auflistung von Zertifikaten fest, die zum Erstellen der Zertifikatkette verwendet werden können, oder ruft sie ab.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: CertificateStatus.Certificates (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b049338bd741281c5b7f012fe4ae7ae443cc2c4b6f9dd7f29591e7616fb8b5dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770387"
---
# <a name="certificatestatuscertificates-property"></a>CertificateStatus.Certificates (Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Certificates-Eigenschaft** legt die Sammlung von Zertifikaten fest, die zum Erstellen der Zertifikatkette verwendet werden können, oder ruft sie ab.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**Certificates-Objekt,**](certificates.md) das die Auflistung von Zertifikaten darstellt, die zum Erstellen der Zertifikatkette verwendet werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.1 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
