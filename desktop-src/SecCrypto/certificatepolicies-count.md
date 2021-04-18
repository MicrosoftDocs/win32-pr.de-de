---
description: Ruft die Anzahl der policyinformation-Objekte in der Auflistung ab.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: Certificatepolicies. Count-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364466"
---
# <a name="certificatepoliciescount-property"></a>Certificatepolicies. Count-Eigenschaft

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Extension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace, indem Sie den Konstruktor aufrufen, der eine OID als Parameter annimmt, und dann die OID für Zertifikat Richtlinien verwenden, um die Zertifikat Richtlinien abzurufen.\]

Die **count** -Eigenschaft ruft die Anzahl der [**policyinformation**](policyinformation.md) -Objekte in der-Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der [**policyinformation**](policyinformation.md) -Objekte in der Auflistung. Jedes **policyinformation** -Objekt stellt eine einzelne Zertifikat Richtlinie in der Sammlung dar.

## <a name="remarks"></a>Bemerkungen

Die **count** -Eigenschaft kann verwendet werden, um das letzte [**policyinformation**](policyinformation.md) -Objekt in der Auflistung anzugeben, wenn ein bestimmtes **policyinformation** -Objekt mithilfe der [**certificatepolicies. Item**](certificatepolicies-item.md) -Eigenschaft abgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
