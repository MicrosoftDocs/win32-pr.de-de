---
description: Ruft einen booleschen Wert ab, der angibt, ob das decipherOnly-Bit festgelegt ist.
ms.assetid: 69d8649d-c7bc-438b-afdd-6c9d2627cd72
title: KeyUsage.IsDecipherOnlyEnabled-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDecipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e46a2d5fb04b54922081bc7c15ab4cfdcbe7536974720d39472ac0af8c64fca5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622310"
---
# <a name="keyusageisdecipheronlyenabled-property"></a>KeyUsage.IsDecipherOnlyEnabled-Eigenschaft

\[Die **IsDecipherOnlyEnabled-Eigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System.Security.Cryptography.X509Certificates-Namespace.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **IsDecipherOnlyEnabled-Eigenschaft** ruft einen booleschen Wert ab, der angibt, ob das decipherOnly-Bit festgelegt ist.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsDecipherOnlyEnabled As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass das decipherOnly-Bit festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
