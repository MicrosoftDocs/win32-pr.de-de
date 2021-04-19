---
description: Erstellt eine Zertifikat Überprüfungs Kette für ein Zertifikat und gibt ein CertificateStatus-Objekt zurück, das den Gültigkeits Status des Zertifikats enthält.
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: 'ICertificate2:: IsValid-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39fec7c1bd2b369ee512834ed1b58b59871d8ae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369399"
---
# <a name="icertificate2isvalid-method"></a>ICertificate2:: IsValid-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **IsValid** -Methode erstellt eine Zertifikat Überprüfungs Kette für ein Zertifikat und gibt ein [**CertificateStatus**](certificatestatus.md) -Objekt zurück, das den Gültigkeits Status des Zertifikats enthält.

## <a name="syntax"></a>Syntax


```VB
Certificate.IsValid()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> <dt>

[**Stellt**](certificate.md)
</dt> </dl>

 

 
