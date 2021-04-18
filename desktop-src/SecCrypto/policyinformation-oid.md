---
description: Ruft die OID der Richtlinie ab. Dies ist die Standard Eigenschaft.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: Policyinformation. Oid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365925"
---
# <a name="policyinformationoid-property"></a>Policyinformation. Oid (Eigenschaft)

\[Die **OID** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um Richtlinien Informationen in der Zertifikat Richtlinien Erweiterung zu verarbeiten.\]

Die **OID** -Eigenschaft ruft die OID der Richtlinie ab. Dies ist die Standard Eigenschaft.

## <a name="syntax"></a>Syntax


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a>Eigenschaftswert

Der Objekt Bezeichner der Richtlinie als [**OID**](oid.md) -Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Policyinformation**](policyinformation.md)
</dt> </dl>

 

 
