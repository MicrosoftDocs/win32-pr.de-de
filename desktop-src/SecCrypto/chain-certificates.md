---
description: Die Eigenschaft Zertifikate Ruft eine Zertifikat Sammlung ab, die die Zertifikate in der Kette darstellt. Dies ist die Standard Eigenschaft.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: 'IChain2:: Zertifikats (Eigenschaft)'
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
ms.openlocfilehash: a166f1d0dfa7f027058be65c3371d5c055cdb7bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366030"
---
# <a name="ichain2certificates-property"></a>IChain2:: Zertifikats (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Chain-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die Eigenschaft **Zertifikate** Ruft eine [**Zertifikat**](certificates.md) Sammlung ab, die die Zertifikate in der Kette darstellt. Dies ist die Standard Eigenschaft.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a>Eigenschaftswert

Eine [**Zertifikat**](certificates.md) Sammlung, die zum Abrufen von Informationen zu jedem Zertifikat in der Kette verwendet wird. Das erste Zertifikat in der zurückgegebenen Auflistung, "Certificate **. Item**(1)", ist das Endzertifikat der Kette. Das letzte Zertifikat in der Sammlung, "Certificate **. Item**" ("**Zertifikate. count**"), ist das Stamm [*Zertifikat*](../secgloss/r-gly.md) der Kette.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
