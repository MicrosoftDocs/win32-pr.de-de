---
description: Ruft einen booleschen Wert ab, der angibt, ob das digitalSignature-Bit festgelegt ist.
ms.assetid: 561eea86-ff23-4a26-adf2-b43009566eaa
title: KeyUsage.IsDigitalSignatureEnabled-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDigitalSignatureEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 963fc78243cf235fe0975fae203e17d1d4f6e71bb909259c7c83acc4fe9e5f07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080650"
---
# <a name="keyusageisdigitalsignatureenabled-property"></a>KeyUsage.IsDigitalSignatureEnabled-Eigenschaft

\[Die **IsDigitalSignatureEnabled-Eigenschaft** ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System.Security.Cryptography.X509Certificates-Namespace.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **IsDigitalSignatureEnabled-Eigenschaft** ruft einen booleschen Wert ab, der angibt, ob das digitalSignature-Bit festgelegt ist.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsDigitalSignatureEnabled As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass das digitalSignature-Bit festgelegt ist.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
