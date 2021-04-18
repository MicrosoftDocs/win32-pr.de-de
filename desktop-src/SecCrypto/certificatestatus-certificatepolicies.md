---
description: Gibt eine OIDs-Auflistung zurück, die die zum Erstellen des Ketten Objekts verwendeten Zertifikat Richtlinien darstellt.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: CertificateStatus. certificatepolicies-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364942"
---
# <a name="certificatestatuscertificatepolicies-method"></a>CertificateStatus. certificatepolicies-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **certificatepolicies** -Methode gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die Zertifikat Richtlinien darstellt, die zum Erstellen des [**Ketten**](chain.md) Objekts verwendet wurden.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine [**OIDs**](oids.md) -Auflistung. Jedes [**OID**](oid.md) -Objekt in der Auflistung stellt eine Zertifikat Richtlinien-OID dar.

## <a name="remarks"></a>Bemerkungen

Fügen Sie der Sammlung Zertifikats Richtlinie hinzu, um die Zertifikat Richtlinien anzugeben, die zum Erstellen der Zertifikats Vertrauenskette verwendet werden sollen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
