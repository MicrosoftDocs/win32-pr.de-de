---
description: Gibt die EKUs-Auflistung für das Zertifikat zurück.
ms.assetid: 64211a00-7d4d-4381-a134-9cd570ed7dbb
title: Extendedkeyusage. EKUs-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 24bcf7b4332e75afad0e21415a7dfe8eb690c32b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355870"
---
# <a name="extendedkeyusageekus-property"></a>Extendedkeyusage. EKUs-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **EKUs** -Eigenschaft gibt die [**EKUs**](ekus.md) -Sammlung für das Zertifikat zurück.

## <a name="syntax"></a>Syntax


```VB
ExtendedKeyUsage.EKUs As EKUs
```



## <a name="property-value"></a>Eigenschaftswert

Die [**EKUs**](ekus.md) -Auflistung, die die [**EKU**](eku.md) -Objekte für das Zertifikat enthält.

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

 

 
