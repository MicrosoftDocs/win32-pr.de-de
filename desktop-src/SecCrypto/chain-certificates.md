---
description: Die Certificates-Eigenschaft ruft eine Certificates-Sammlung ab, die die Zertifikate in der Kette darstellt. Dies ist die Standardeigenschaft.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: IChain2::Certificates(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 16fb08d020dcd59ed7caf22a0e93f4a4866b58642f12d0c131f3f0368bd3e7e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769651"
---
# <a name="ichain2certificates-property"></a>IChain2::Certificates(Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Certificates-Eigenschaft** ruft eine [**Certificates-Sammlung**](certificates.md) ab, die die Zertifikate in der Kette darstellt. Dies ist die Standardeigenschaft.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a>Eigenschaftswert

Eine [**Zertifikatsammlung,**](certificates.md) die zum Abrufen von Informationen zu jedem Zertifikat in der Kette verwendet wird. Das erste Zertifikat in der zurückgegebenen Sammlung, **Certificates.Item**(1), ist das Endzertifikat der Kette. Das letzte Zertifikat in der Sammlung, **Certificates.Item**(**Certificates.Count**), ist das [*Stammzertifikat*](../secgloss/r-gly.md) der Kette.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
