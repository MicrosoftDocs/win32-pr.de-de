---
description: Ruft eine hexadezimale Zeichenfolge ab, die den SHA-1-Hash des Zertifikats enthält.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Certificate.Thumbprint (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 64748f3eb8b9623ea7c07a7428f29b30276c34ab38631fdbf210b25b5be92a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878160"
---
# <a name="certificatethumbprint-property"></a>Certificate.Thumbprint (Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Thumbprint-Eigenschaft** ruft eine hexadezimale Zeichenfolge ab, die den [*SHA-1-Hash*](../secgloss/s-gly.md) des Zertifikats enthält.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a>Eigenschaftswert

Eine hexadezimale Zeichenfolge, die den SHA-1-Hash des Zertifikats enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zertifikat**](certificate.md)
</dt> </dl>

 

 
