---
description: Gibt eine OIDs-Auflistung zurück, die die Zum Erstellen des Chain-Objekts verwendeten Anwendungsrichtlinien darstellt.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: CertificateStatus.ApplicationPolicies-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a27bc08f658e317b41380b2dabd9aadc13e8b50bd4985c0fd13211fa81fd507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770440"
---
# <a name="certificatestatusapplicationpolicies-method"></a>CertificateStatus.ApplicationPolicies-Methode

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **ApplicationPolicies-Methode** gibt eine [**OIDs-Auflistung**](oids.md) zurück, die die Anwendungsrichtlinien darstellt, die zum Erstellen des [**Chain-Objekts**](chain.md) verwendet werden.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine [**OIDs-Auflistung.**](oids.md) Jedes [**OID-Objekt**](oid.md) in der Auflistung stellt eine Anwendungsrichtlinien-OID dar.

## <a name="remarks"></a>Hinweise

Fügen Sie der Sammlung Anwendungsrichtlinien-OIDs hinzu, um die Anwendungsrichtlinien anzugeben, die zum Erstellen der Zertifikatvertrauenskette verwendet werden sollen. Wenn die Auflistung mindestens ein [**OID-Objekt**](oid.md) enthält, wird das von der [**CertificateStatus.EKU-Methode**](certificatestatus-eku.md) zurückgegebene [**EKU-Objekt**](eku.md) ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
