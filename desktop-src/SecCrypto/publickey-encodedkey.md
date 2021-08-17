---
description: Ruft den Wert des öffentlichen Schlüssels ab.
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: PublicKey.EncodedKey-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0d4708461f5ff51d5f86170ba0f1df35669859149b4882f8fb86aafdbed5e436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901462"
---
# <a name="publickeyencodedkey-property"></a>PublicKey.EncodedKey-Eigenschaft

\[Die **Eigenschaft EncodedKey** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2.PublicKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **EncodedKey-Eigenschaft** ruft den Wert des öffentlichen Schlüssels ab.

## <a name="syntax"></a>Syntax


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**EncodedData-Objekt,**](encodeddata.md) das Zugriff auf den Wert des öffentlichen Schlüssels bietet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Publickey**](publickey.md)
</dt> </dl>

 

 
