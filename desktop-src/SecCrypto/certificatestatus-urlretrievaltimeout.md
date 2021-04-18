---
description: Legt die Zeitspanne fest, nach der eine URL als nicht erreichbar festgelegt wird, oder ruft Sie ab.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: CertificateStatus. UrlRetrievalTimeout-Eigenschaft
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
ms.openlocfilehash: fcaaafa1f2e870195b612eb225696f2c23a80ee1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365376"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a>CertificateStatus. UrlRetrievalTimeout-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **UrlRetrievalTimeout** -Eigenschaft legt die Zeitspanne fest, nach der eine URL als nicht erreichbar festgelegt wird, oder ruft Sie ab.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der Sekunden, bevor eine URL als nicht erreichbar festgelegt wird.

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft nicht festgelegt ist, beträgt das Standard Timeout 15 Sekunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
