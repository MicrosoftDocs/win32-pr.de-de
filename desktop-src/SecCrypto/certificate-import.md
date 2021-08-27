---
description: Importiert ein zuvor codiertes Zertifikat aus einer Zeichenfolge in das Certificate-Objekt.
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: ICertificate2::Import-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1f47ebe884c8fb3a10a8ebdef89353e7549c916a7793075d0086d2f0cd2ce717
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127010"
---
# <a name="icertificate2import-method"></a>ICertificate2::Import-Methode

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **Import-Methode** importiert ein zuvor codiertes Zertifikat aus einer Zeichenfolge in das [**Certificate-Objekt.**](certificate.md) Durch Aufrufen dieser Methode wird der [*Zustand*](../secgloss/s-gly.md) dieses Objekts zurückgesetzt.

## <a name="syntax"></a>Syntax


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EncodedCertificate* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die die zu importierenden codierten Zertifikatdaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kryptografieobjekte](cryptography-objects.md)
</dt> <dt>

[**Zertifikat**](certificate.md)
</dt> </dl>

 

 
