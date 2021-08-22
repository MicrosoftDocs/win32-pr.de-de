---
description: Gibt einen booleschen Wert zurück, der angibt, ob die EKU-Erweiterung vorhanden ist. Dies ist die Standardeigenschaft.
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: ExtendedKeyUsage.IsPresent-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43c561e6c848380326151af12aebf584fb53eb7332c8e6c0d61074da03f7d3de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007338"
---
# <a name="extendedkeyusageispresent-property"></a>ExtendedKeyUsage.IsPresent-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System.Security.Cryptography.X509Certificates-Namespace.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **IsPresent-Eigenschaft** gibt einen booleschen Wert zurück, der angibt, ob die EKU-Erweiterung vorhanden ist. Dies ist die Standardeigenschaft.

## <a name="syntax"></a>Syntax


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass die EKU-Erweiterung vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ExtendedKeyUsage**](extendedkeyusage.md)
</dt> </dl>

 

 
