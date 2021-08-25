---
description: Ruft einen booleschen Wert ab, der angibt, ob das Zertifikat für eine Zertifizierungsstelle (Ca) vorgesehen ist.
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: BasicConstraints.IsCertificateAuthority-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 90d616f4a7a0fe8522118848826bee88523ad45c34cb8a3fff23c722e68f2495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879760"
---
# <a name="basicconstraintsiscertificateauthority-property"></a>BasicConstraints.IsCertificateAuthority-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**X509BasicConstraintsExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) im [**System.Security.Cryptography.X509Certificates-Namespace.**](/previous-versions/windows/)\]

Die **IsCertificateAuthority-Eigenschaft** ruft einen booleschen Wert ab, der angibt, ob das Zertifikat für eine [*Zertifizierungsstelle*](../secgloss/c-gly.md) (Ca) vorgesehen ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

**True** gibt an, dass das Zertifikat nur von einer Zertifizierungsstelle verwendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
