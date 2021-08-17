---
description: Legt den privaten Schlüssel fest, der dem Zertifikat zugeordnet ist, oder ruft diesen ab.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Certificate.PrivateKey(Eigenschaft)
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
ms.openlocfilehash: 18e6acc2aa4b765e9219eff479280df814f1089dc27366c5d175dcdeda4fd890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771555"
---
# <a name="certificateprivatekey-property"></a>Certificate.PrivateKey(Eigenschaft)

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **PrivateKey-Eigenschaft** legt den privaten Schlüssel fest, der dem Zertifikat zugeordnet ist, oder ruft diesen ab. Diese Eigenschaft wurde in CAPICOM 2.0 eingeführt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**PrivateKey-Objekt,**](privatekey.md) das den privaten Schlüssel darstellt, der dem Zertifikat zugeordnet ist.

## <a name="remarks"></a>Hinweise

Wenn Sie **die PrivateKey-Eigenschaft** auf Nothing festlegen, wird die Zuordnung zwischen dem privaten Schlüssel und dem Zertifikat entfernt, aber der private Schlüssel wird nicht gelöscht. Um den privaten Schlüssel zu löschen, rufen Sie die [**PrivateKey.Delete-Methode**](privatekey-delete.md) auf, und legen Sie diese Eigenschaft dann auf Nothing fest.

Diese Eigenschaft löst CAPICOM \_ E \_ NOT ALLOWED \_ aus, wenn sie von einer webbasierten Anwendung festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Zertifikat**](certificate.md)
</dt> </dl>

 

 
