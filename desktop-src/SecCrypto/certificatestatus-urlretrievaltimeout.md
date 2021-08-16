---
description: Legt die Zeitdauer fest oder ruft sie ab, bevor eine URL als nicht erreichbar bestimmt wird.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: CertificateStatus.UrlRetrievalTimeout (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b56e9bca2cc7c666f980df8905ac79fc885050d37359e524a83e287dcd5415e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770090"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a>CertificateStatus.UrlRetrievalTimeout (Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **UrlRetrievalTimeout-Eigenschaft** legt die Zeitdauer fest oder ruft sie ab, bevor eine URL als nicht erreichbar bestimmt wird.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl von Sekunden, bevor festgestellt wird, dass eine URL nicht erreichbar ist.

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft nicht festgelegt ist, beträgt das Standard-Time out 15 Sekunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
