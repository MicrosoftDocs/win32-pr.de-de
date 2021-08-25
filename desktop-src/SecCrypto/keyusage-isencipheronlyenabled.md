---
description: Ruft einen booleschen Wert ab, der angibt, ob das encipherOnly-Bit festgelegt ist.
ms.assetid: 60d79ea4-4968-49e0-8d16-873fbcbd951c
title: KeyUsage.IsEncipherOnlyEnabled-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsEncipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 30b786eda3655a1fabe8c16b6fb3ce2f7a0c597547903019d7027ada5f446ea6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867670"
---
# <a name="keyusageisencipheronlyenabled-property"></a>KeyUsage.IsEncipherOnlyEnabled-Eigenschaft

\[Die **IsEncipherOnlyEnabled-Eigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System.Security.Cryptography.X509Certificates-Namespace.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **IsEncipherOnlyEnabled-Eigenschaft** ruft einen booleschen Wert ab, der angibt, ob das encipherOnly-Bit festgelegt ist.

## <a name="syntax"></a>Syntax


```VB
KeyUsage.IsEncipherOnlyEnabled As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt an, dass das encipherOnly-Bit festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**KeyUsage**](keyusage.md)
</dt> </dl>

 

 
