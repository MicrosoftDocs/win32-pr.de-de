---
description: Ruft das Enddatum für die Gültigkeit des Zertifikats ab.
ms.assetid: 25e76b25-9a18-439c-acb8-e0af97b6fcd5
title: Certificate.ValidToDate-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ValidToDate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a94e061719dc221cedf2f086648677373c9dd7b72d1619b22bb288b484534de9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126790"
---
# <a name="certificatevalidtodate-property"></a>Certificate.ValidToDate-Eigenschaft

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **ValidToDate-Eigenschaft** ruft das Enddatum für die Gültigkeit des Zertifikats ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
Certificate.ValidToDate As Date
```



## <a name="property-value"></a>Eigenschaftswert

Ein Datum, das das Enddatum für die Gültigkeit des Zertifikats angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zertifikat**](certificate.md)
</dt> </dl>

 

 
