---
description: Die algorithmuseigenschaft Ruft das Oid-Objekt ab, das den Algorithmus identifiziert, der vom öffentlichen Schlüssel verwendet wird. Dies ist die Standard Eigenschaft.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: PublicKey. algorithmuseigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366742"
---
# <a name="publickeyalgorithm-property"></a>PublicKey. algorithmuseigenschaft

\[Die **algorithmuseigenschaft** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Certificate2. PublicKey-Eigenschaft**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die  algorithmuseigenschaft Ruft das [**OID**](oid.md) -Objekt ab, das den Algorithmus identifiziert, der vom öffentlichen Schlüssel verwendet wird. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a>Eigenschaftswert

Das [**OID**](oid.md) -Objekt, das den vom öffentlichen Schlüssel verwendeten Algorithmus identifiziert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
