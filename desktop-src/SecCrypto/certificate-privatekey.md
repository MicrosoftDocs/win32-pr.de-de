---
description: Legt den privaten Schlüssel fest, der dem Zertifikat zugeordnet ist, oder ruft ihn ab.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Certificate. PrivateKey (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370954"
---
# <a name="certificateprivatekey-property"></a>Certificate. PrivateKey (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **PrivateKey** -Eigenschaft legt den dem Zertifikat zugeordneten privaten Schlüssel fest oder ruft ihn ab. Diese Eigenschaft wurde in CAPICOM 2,0 eingeführt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**PrivateKey**](privatekey.md) -Objekt, das den privaten Schlüssel darstellt, der dem Zertifikat zugeordnet ist.

## <a name="remarks"></a>Bemerkungen

Wenn die **PrivateKey** -Eigenschaft auf "Nothing" festgelegt wird, wird die Zuordnung zwischen dem privaten Schlüssel und dem Zertifikat entfernt. der private Schlüssel wird jedoch nicht gelöscht. Um den privaten Schlüssel zu löschen, nennen Sie die [**PrivateKey. Delete**](privatekey-delete.md) -Methode, und legen Sie diese Eigenschaft auf "Nothing" fest.

Diese Eigenschaft löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn Sie von einer webbasierten Anwendung aus festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Stellt**](certificate.md)
</dt> </dl>

 

 
