---
description: Gibt ein ExtendedKeyUsage-Objekt zurück, das die gültigen Verwendungsmöglichkeiten des Zertifikats angibt.
ms.assetid: e974e9e2-1011-48b7-9ebc-e754e4990286
title: ICertificate2::ExtendedKeyUsage-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ExtendedKeyUsage
- ICertificate2.ExtendedKeyUsage
- ICertificate.ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c496faf8c28c6dc9abacf75156f53a91cf7fc4d71b4ef469b64d2daa424d1a01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771654"
---
# <a name="icertificate2extendedkeyusage-method"></a>ICertificate2::ExtendedKeyUsage-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **ExtendedKeyUsage-Methode** gibt ein [**ExtendedKeyUsage-Objekt**](extendedkeyusage.md) zurück, das die gültigen Verwendungsmöglichkeiten des Zertifikats angibt.

## <a name="syntax"></a>Syntax


```VB
Certificate.ExtendedKeyUsage()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Das [**ExtendedKeyUsage-Objekt,**](extendedkeyusage.md) das dem Zertifikat zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> <dt>

[**Zertifikat**](certificate.md)
</dt> </dl>

 

 
