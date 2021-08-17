---
description: Ruft ein Certificate-Objekt ab, das das indizierte Zertifikat der Auflistung darstellt. Dies ist die Standardeigenschaft.
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Certificates.Item-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 927f52570b515c6699458cfb802b5c315201d401e9bcf5e0be76ab41863bd47e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770539"
---
# <a name="certificatesitem-property"></a>Certificates.Item-Eigenschaft

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Item-Eigenschaft** ruft ein [**Certificate-Objekt ab,**](certificate.md) das das indizierte Zertifikat der Auflistung darstellt. Dies ist die Standardeigenschaft.

## <a name="syntax"></a>Syntax


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**Certificate-Objekt,**](certificate.md) das das indizierte Zertifikat darstellt.

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

 

 
