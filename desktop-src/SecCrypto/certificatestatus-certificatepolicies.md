---
description: Gibt eine OIDs-Auflistung zurück, die die Zertifikatrichtlinien darstellt, die zum Erstellen des Chain-Objekts verwendet werden.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: CertificateStatus.CertificatePolicies-Methode
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
ms.openlocfilehash: e4d6507446bf15d00d8e388699ee0c0892c8755b94913d18657634311db57ec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126710"
---
# <a name="certificatestatuscertificatepolicies-method"></a>CertificateStatus.CertificatePolicies-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **CertificatePolicies-Methode** gibt eine [**OIDs-Auflistung zurück,**](oids.md) die die Zertifikatrichtlinien darstellt, die zum Erstellen des [**Chain-Objekts verwendet**](chain.md) werden.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine [**OIDs-Auflistung.**](oids.md) Jedes [**OID-Objekt**](oid.md) in der Auflistung stellt eine Zertifikatrichtlinien-OID dar.

## <a name="remarks"></a>Hinweise

Fügen Sie der Sammlung Zertifikatrichtlinien-OIDs hinzu, um die Zertifikatrichtlinien anzugeben, die zum Erstellen der Zertifikatvertrauenskette verwendet werden sollen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
