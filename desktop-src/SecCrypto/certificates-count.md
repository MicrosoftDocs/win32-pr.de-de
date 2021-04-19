---
description: Ruft die Anzahl der Zertifikat Objekte in der Auflistung ab.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Zertifikats. Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a67554530ce8c8dfdc1bfcfba1198cf778397ac2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361504"
---
# <a name="certificatescount-property"></a>Zertifikats. Count-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2Collection-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **count** -Eigenschaft ruft die Anzahl der [**Zertifikat**](certificate.md) Objekte in der Auflistung ab.

## <a name="syntax"></a>Syntax


```VB
Certificates.Count As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der [**Zertifikat**](certificate.md) Objekte in der Auflistung. Jedes **Zertifikat** Objekt stellt ein einzelnes Zertifikat in der Sammlung dar.

## <a name="remarks"></a>Bemerkungen

CAPICOM unterstützt nur ein einzelnes Zertifikat für den [*smartcardspeicher*](../secgloss/s-gly.md) . Auch wenn der smartcardspeicher mehr als ein Zertifikat enthält, enthält diese Eigenschaft den Wert 1. Weitere Informationen zum smartcardspeicher finden Sie unter dem **CAPICOM- \_ \_ Smartcard- \_ Benutzer \_ Speicher** Mitglied der " [**CAPICOM \_ Store \_ Location**](capicom-store-location.md) "-Enumeration.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zertifikate**](certificates.md)
</dt> </dl>

 

 
