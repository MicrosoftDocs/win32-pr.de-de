---
description: Ruft das Anfangsdatum für die Gültigkeit des Zertifikats ab.
ms.assetid: d1caa7d3-ed5c-4637-bcb6-5a3fda8b978e
title: Certificate. validfromdate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ValidFromDate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8637114ad471b2d938a94ba2d974703bdfb1f5d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361496"
---
# <a name="certificatevalidfromdate-property"></a>Certificate. validfromdate (Eigenschaft)

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **validfromdate** -Eigenschaft ruft das Anfangsdatum für die Gültigkeit des Zertifikats ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Certificate.ValidFromDate As Date
```



## <a name="property-value"></a>Eigenschaftswert

Ein Datum, das das Anfangsdatum für die Gültigkeit des Zertifikats angibt.

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

 

 
