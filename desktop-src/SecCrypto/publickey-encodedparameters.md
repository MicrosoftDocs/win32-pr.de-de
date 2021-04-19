---
description: Ruft die Parameter des Algorithmus des öffentlichen Schlüssels ab.
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: PublicKey. EncodedParameters (Eigenschaft)
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
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366741"
---
# <a name="publickeyencodedparameters-property"></a>PublicKey. EncodedParameters (Eigenschaft)

\[Die **EncodedParameters** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2. PublicKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **EncodedParameters** -Eigenschaft ruft die Parameter des Algorithmus des öffentlichen Schlüssels ab.

## <a name="syntax"></a>Syntax


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**encodeddata**](encodeddata.md) -Objekt, das Zugriff auf die Parameter des Algorithmus des öffentlichen Schlüssels bereitstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
