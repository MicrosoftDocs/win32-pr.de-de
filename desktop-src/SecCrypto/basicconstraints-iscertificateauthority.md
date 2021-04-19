---
description: Ruft einen booleschen Wert ab, der angibt, ob das Zertifikat für eine Zertifizierungsstelle (Certification Authority, ca) gilt.
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: Basiceinschränkungs. iscertificateauthority (Eigenschaft)
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
ms.openlocfilehash: 5d4878a8cb21f89f3abeeb9e4b530948ef12e9aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361409"
---
# <a name="basicconstraintsiscertificateauthority-property"></a>Basiceinschränkungs. iscertificateauthority (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**X509BasicConstraintsExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) -Namespace.\]

Die **iscertificateauthority** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob das Zertifikat für eine Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) gilt.

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
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
