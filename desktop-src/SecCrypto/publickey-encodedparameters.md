---
description: Ruft die Parameter des Algorithmus für öffentliche Schlüssel ab.
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: PublicKey.EncodedParameters(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a28fff75b293189d207dcf8cbec6757a436e75e76163841b3cb51bfa856bf8bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117976104"
---
# <a name="publickeyencodedparameters-property"></a>PublicKey.EncodedParameters(Eigenschaft)

\[Die **Eigenschaft EncodedParameters** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2.PublicKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Eigenschaft EncodedParameters** ruft die Parameter des Algorithmus für öffentliche Schlüssel ab.

## <a name="syntax"></a>Syntax


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**EncodedData-Objekt,**](encodeddata.md) das Zugriff auf die Parameter des Algorithmus für öffentliche Schlüssel bietet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Publickey**](publickey.md)
</dt> </dl>

 

 
