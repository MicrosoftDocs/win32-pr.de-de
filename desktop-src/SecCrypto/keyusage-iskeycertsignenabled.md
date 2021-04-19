---
description: Ruft einen booleschen Wert ab, der angibt, ob das keyCertSign-Bit festgelegt ist.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: KeyUsage. iskeycertsignenabled (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyCertSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d475565896910f76211e3843526e9a889586efa0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355253"
---
# <a name="keyusageiskeycertsignenabled-property"></a>KeyUsage. iskeycertsignenabled (Eigenschaft)

\[Die **iskeycertsignenabled** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **iskeycertsignenabled** -Eigenschaft ruft einen booleschen Wert ab, der angibt, ob das keyCertSign-Bit festgelegt ist.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

**True** gibt an, dass das keyCertSign-Bit festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Endeinheits Zertifikaten der**](keyusage.md)
</dt> </dl>

 

 
