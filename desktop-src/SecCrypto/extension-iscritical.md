---
description: Ruft einen booleschen Wert ab, der angibt, ob die Erweiterung als kritisch markiert ist.
ms.assetid: 71f55d63-a51c-472c-81fc-59212c97bb34
title: Erweiterung. IsCritical (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 61e53f869a7063e029cb629b8b2fff4cff025b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356401"
---
# <a name="extensioniscritical-property"></a>Erweiterung. IsCritical (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **IsCritical** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob die Erweiterung als kritisch markiert ist.

## <a name="syntax"></a>Syntax


```VB
Extension.IsCritical As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

**True** gibt an, dass die Erweiterung als kritisch markiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
