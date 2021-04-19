---
description: Gibt einen booleschen Wert zurück, der angibt, ob die EKU-Erweiterung vorhanden ist. Dies ist die Standard Eigenschaft.
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: Extendedkeyusage. ispree sent (Eigenschaft)
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
ms.openlocfilehash: 785fa3c973e7f90eeab20bd76826b9e5bf612891
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367691"
---
# <a name="extendedkeyusageispresent-property"></a>Extendedkeyusage. ispree sent (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **ispree sent** -Eigenschaft gibt einen booleschen Wert zurück, der angibt, ob die EKU-Erweiterung vorhanden ist. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

**True** gibt an, dass die EKU-Erweiterung vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Extendedkeyusage**](extendedkeyusage.md)
</dt> </dl>

 

 
