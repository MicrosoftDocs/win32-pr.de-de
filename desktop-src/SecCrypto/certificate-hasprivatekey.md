---
description: Bestimmt, ob dem Zertifikat ein privater Schlüssel zugeordnet ist. Die-Methode bestimmt dies, indem Sie überprüft, ob die \_ Eigenschaft Zertifikat Schlüssel \_ Prov \_ Info \_ Prop \_ ID vorhanden ist.
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: 'ICertificate2:: HasPrivateKey-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43110e48a1172977ad979d6ec2d94c5b8e3ffc50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353827"
---
# <a name="icertificate2hasprivatekey-method"></a>ICertificate2:: HasPrivateKey-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **HasPrivateKey** -Methode bestimmt, ob dem [*Zertifikat*](../secgloss/c-gly.md) ein [*privater Schlüssel*](../secgloss/p-gly.md) zugeordnet ist. Die-Methode bestimmt dies, indem Sie überprüft, ob die \_ Eigenschaft Zertifikat Schlüssel \_ Prov \_ Info \_ Prop \_ ID vorhanden ist.

## <a name="syntax"></a>Syntax


```VB
Certificate.HasPrivateKey()
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

[**PrivateKey. Open**](privatekey-open.md)
</dt> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> <dt>

[**Stellt**](certificate.md)
</dt> </dl>

 

 
