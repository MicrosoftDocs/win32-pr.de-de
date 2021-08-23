---
description: Ruft einen booleschen Wert ab, der angibt, ob das keyCertSign-Bit festgelegt ist.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: KeyUsage.IsKeyCertSignEnabled (Eigenschaft)
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
ms.openlocfilehash: 61c5ca1e9ae36159293e1e9afe1f79b5ff30cbd659b01a400797ae35aac8873c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515880"
---
# <a name="keyusageiskeycertsignenabled-property"></a>KeyUsage.IsKeyCertSignEnabled (Eigenschaft)

\[Die **IsKeyCertSignEnabled-Eigenschaft** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **IsKeyCertSignEnabled-Eigenschaft** ruft einen booleschen Wert ab, der angibt, ob das keyCertSign-Bit festgelegt ist.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True **gibt an,** dass das keyCertSign-Bit festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
