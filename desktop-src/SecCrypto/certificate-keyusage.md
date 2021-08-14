---
description: Gibt ein KeyUsage-Objekt zurück, das die gültige Schlüsselverwendung des Zertifikats angibt.
ms.assetid: e4590e95-ffa2-4953-bfc1-4d7c70271029
title: ICertificate2::KeyUsage-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.KeyUsage
- ICertificate2.KeyUsage
- ICertificate.KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7ce3fc7246a7962ea852167cdc93e25e4d8ab11976eb3cf2868642bb906c41fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771533"
---
# <a name="icertificate2keyusage-method"></a>ICertificate2::KeyUsage-Methode

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **KeyUsage-Methode** gibt ein [**KeyUsage-Objekt**](keyusage.md) zurück, das die gültige Schlüsselverwendung des Zertifikats angibt.

## <a name="syntax"></a>Syntax


```VB
Certificate.KeyUsage()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

 

 
