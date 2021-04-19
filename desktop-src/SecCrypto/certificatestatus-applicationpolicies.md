---
description: Gibt eine OIDs-Auflistung zurück, die die Anwendungsrichtlinien darstellt, die zum Erstellen des Ketten Objekts verwendet werden.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: CertificateStatus. applicationpolicies-Methode
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
ms.openlocfilehash: b02503590a64c1c14e3f66dc5d07d9d61034bd60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354082"
---
# <a name="certificatestatusapplicationpolicies-method"></a>CertificateStatus. applicationpolicies-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **applicationpolicies** -Methode gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die Anwendungsrichtlinien darstellt, die zum Erstellen des [**Ketten**](chain.md) Objekts verwendet werden.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine [**OIDs**](oids.md) -Auflistung. Jedes [**OID**](oid.md) -Objekt in der Auflistung stellt eine Anwendungsrichtlinien-OID dar.

## <a name="remarks"></a>Bemerkungen

Fügen Sie der Sammlung Anwendungsrichtlinien-OIDs hinzu, um die Anwendungsrichtlinien anzugeben, die zum Erstellen der Zertifikats Vertrauenskette verwendet werden sollen. Wenn die Auflistung mindestens ein [**OID**](oid.md) -Objekt enthält, wird das von der [**CertificateStatus. EKU**](certificatestatus-eku.md) -Methode zurückgegebene [**EKU**](eku.md) -Objekt ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
