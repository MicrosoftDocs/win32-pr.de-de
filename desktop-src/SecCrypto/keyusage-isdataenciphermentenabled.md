---
description: Ruft einen booleschen Wert ab, der angibt, ob das DataEncipherment-Bit festgelegt ist.
ms.assetid: 9b29a76f-1494-4db3-a5d7-69fe631ca1dd
title: KeyUsage. isdataenciphermentaktivierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDataEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aad6cbcd21830ad127b9537749dfb1c05a4c9ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355255"
---
# <a name="keyusageisdataenciphermentenabled-property"></a>KeyUsage. isdataenciphermentaktivierte Eigenschaft

\[Die **isdataenciphermentaktivierte** Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **isdataenciphermentaktivierte** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob das DataEncipherment-Bit festgelegt ist.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsDataEnciphermentEnabled As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

**True** gibt an, dass das DataEncipherment-Bit festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Endeinheits Zertifikaten der**](keyusage.md)
</dt> </dl>

 

 
