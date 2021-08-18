---
description: Ruft die codierten Daten für die Erweiterung ab.
ms.assetid: 79811557-6d7e-4d19-bcbb-1f79455dd286
title: Extension.EncodedData-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4783a6f598bf094ca2bca10b2abcb7e222e34ffc5956b2dc6f0977416e9e99a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006948"
---
# <a name="extensionencodeddata-property"></a>Extension.EncodedData-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **EncodedData-Eigenschaft** ruft die codierten Daten für die Erweiterung ab.

## <a name="syntax"></a>Syntax


```VB
Extension.EncodedData As EncodedData
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**EncodedData-Objekt,**](encodeddata.md) das die Daten der Zertifikaterweiterung darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
