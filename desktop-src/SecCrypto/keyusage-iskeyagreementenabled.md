---
description: Ruft einen booleschen Wert ab, der angibt, ob das keyAgreement-Bit festgelegt ist.
ms.assetid: 3dd1f6c7-893d-453e-92dc-ffeffd879519
title: KeyUsage.IsKeyAgreementEnabled (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyAgreementEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5e70c065bbdf3f3ba53b9adef410b4462d06251201281ef6946c52ed9d92f27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408770"
---
# <a name="keyusageiskeyagreementenabled-property"></a>KeyUsage.IsKeyAgreementEnabled (Eigenschaft)

\[Die **IsKeyAgreementEnabled-Eigenschaft** ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **IsKeyAgreementEnabled-Eigenschaft** ruft einen booleschen Wert ab, der angibt, ob das keyAgreement-Bit festgelegt ist.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsKeyAgreementEnabled As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True **gibt an,** dass das keyAgreement-Bit festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
