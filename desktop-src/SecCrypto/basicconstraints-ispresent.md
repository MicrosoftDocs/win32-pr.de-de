---
description: Ruft einen booleschen Wert ab, der angibt, ob die Basiseinschränkungserweiterung vorhanden ist. Dies ist die Standardeigenschaft.
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: BasicConstraints.IsPresent-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 646d7988b24d9ad03e55bb7ee4401875c42f7b779a81e1b80a611aaae18a93a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773022"
---
# <a name="basicconstraintsispresent-property"></a>BasicConstraints.IsPresent-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista, Windows XP. Verwenden Sie stattdessen die [**X509BasicConstraintsExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) im [**System.Security.Cryptography.X509Certificates-Namespace.**](/previous-versions/windows/)\]

Die **IsPresent-Eigenschaft** ruft einen booleschen Wert ab, der angibt, ob die Erweiterung für grundlegende Einschränkungen vorhanden ist. Dies ist die Standardeigenschaft.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass die Grundlegende Einschränkungserweiterung vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BasicConstraints**](basicconstraints.md)
</dt> </dl>

 

 
