---
description: Legt das Zertifikat Objekt fest, das das Zertifikat eines Signatur Gebers der Daten darstellt, oder ruft es ab.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Signer. Certificate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367438"
---
# <a name="signercertificate-property"></a>Signer. Certificate (Eigenschaft)

\[Die **Zertifikat** Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**CmsSigner-Klasse**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) im [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) -Namespace.\]

Die **Certificate** -Eigenschaft legt das [**Zertifikat**](certificate.md) Objekt fest oder ruft es ab, das das Zertifikat eines Signatur Gebers für die Daten darstellt. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a>Eigenschaftswert

Das [**Zertifikat**](certificate.md) Objekt, das das Zertifikat eines Signatur Gebers der Daten darstellt.

## <a name="remarks"></a>Bemerkungen

Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Signatur Geber**](signer.md)
</dt> </dl>

 

 
