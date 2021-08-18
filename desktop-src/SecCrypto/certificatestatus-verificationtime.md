---
description: Legt den Zeitpunkt fest, zu dem das Zertifikat überprüft wurde, oder ruft diesen ab.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: CertificateStatus.VerificationTime (Eigenschaft)
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
ms.openlocfilehash: 02457355fdb9f01605470ea10e30d69caaa6149837480ebe7bd20340d7c6cae2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993150"
---
# <a name="certificatestatusverificationtime-property"></a>CertificateStatus.VerificationTime (Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **VerificationTime-Eigenschaft** legt den Zeitpunkt fest, zu dem das Zertifikat überprüft wurde, oder ruft diesen ab.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a>Eigenschaftswert

Der Zeitpunkt, zu dem das Zertifikat überprüft wurde.

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft nicht festgelegt ist, wird die aktuelle Zeit verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
