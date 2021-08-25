---
description: Ruft den Verschlüsselungsalgorithmus und die Schlüssellänge ab.
ms.assetid: 13b2a3db-f04b-4436-b64f-f194fc9ddac2
title: EnvelopedData.Algorithm-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 58971f27c271e18cef63f670a74ad0b78bbcb92914d35d9c6ca1f8461dfe15ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874410"
---
# <a name="envelopeddataalgorithm-property"></a>EnvelopedData.Algorithm-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**EnvelopedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System.Security.Cryptography.Pkcs-Namespace.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

Die **Algorithm-Eigenschaft** ruft den Verschlüsselungsalgorithmus und die [*Schlüssellänge*](../secgloss/k-gly.md)ab.

## <a name="syntax"></a>Syntax


```VB
EnvelopedData.Algorithm As Algorithm
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**Algorithm-Objekt,**](algorithm.md) das den Verschlüsselungsalgorithmus und die Schlüssellänge enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
