---
description: Ruft den Wert des öffentlichen Schlüssels ab.
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: PublicKey. encodecodkey (Eigenschaft)
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
ms.openlocfilehash: de2c7b2bfbbdaf28345ae29e260bfd30c5754ffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370817"
---
# <a name="publickeyencodedkey-property"></a>PublicKey. encodecodkey (Eigenschaft)

\[Die **encodedkey** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2. PublicKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **encodecodkey** -Eigenschaft ruft den Wert des öffentlichen Schlüssels ab.

## <a name="syntax"></a>Syntax


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**encoddata**](encodeddata.md) -Objekt, das Zugriff auf den Wert des öffentlichen Schlüssels bereitstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
