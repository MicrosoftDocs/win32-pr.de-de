---
description: Ruft die dem SignedData-Objekt zugeordnete Zertifikats Auflistung ab. Nach dem abrufen können die einzelnen Zertifikat Objekte in der Auflistung aufgelistet werden.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: SignedData. Zertifikats (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354162"
---
# <a name="signeddatacertificates-property"></a>SignedData. Zertifikats (Eigenschaft)

\[Die Eigenschaft **Zertifikate** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Verwenden Sie stattdessen die [**SignedCms-Klasse**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Mit der Eigenschaft **Zertifikate** wird die dem [**SignedData**](signeddata.md) -Objekt zugeordnete [**Zertifikats**](certificates.md) Sammlung abgerufen. Nach dem abrufen können die einzelnen [**Zertifikat**](certificate.md) Objekte in der Auflistung aufgelistet werden.

## <a name="syntax"></a>Syntax


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a>Eigenschaftswert

Die dem [**SignedData**](signeddata.md) -Objekt zugeordnete [**Zertifikats**](certificates.md) Auflistung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
