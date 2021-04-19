---
description: Legt die Uhrzeit fest, zu der das Zertifikat überprüft wurde, oder ruft diese ab.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: CertificateStatus. VerificationTime-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350756"
---
# <a name="certificatestatusverificationtime-property"></a>CertificateStatus. VerificationTime-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **VerificationTime** -Eigenschaft legt die Uhrzeit fest, zu der das Zertifikat überprüft wurde, oder ruft diese ab.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a>Eigenschaftswert

Der Zeitpunkt, zu dem das Zertifikat überprüft wurde.

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft nicht festgelegt ist, wird die aktuelle Uhrzeit verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
