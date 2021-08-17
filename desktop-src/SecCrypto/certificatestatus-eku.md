---
description: Gibt das EKU-Objekt zurück, das zum Erstellen des Chain-Objekts verwendet wird.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: CertificateStatus.EKU-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 63ddc2cd793c786cff1f7c5bb983cdba525fb52f940723f826ab4b44b89bf1ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770290"
---
# <a name="certificatestatuseku-method"></a>CertificateStatus.EKU-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Die **EKU-Methode** gibt das [**EKU-Objekt**](eku.md) zurück, das zum Erstellen des [**Chain-Objekts verwendet**](chain.md) wird.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein [**EKU-Objekt**](eku.md) zurück, das die erweiterte Schlüsselverwendungseinstellung des Zertifikats [*angibt.*](../secgloss/c-gly.md) Die EKU-Einstellung legt die gültige Verwendung eines Zertifikats fest. Für jedes Zertifikat kann nur ein einzelnes **EKU-Objekt** festgelegt werden.

## <a name="remarks"></a>Hinweise

Die [**CertificateStatus.ApplicationPolicies-Methode**](certificatestatus-applicationpolicies.md) bietet die gleiche Funktionalität wie diese Methode, lässt jedoch zu, dass viele Einstellungen anstelle von nur einer angegeben werden können. Wenn die von der **ApplicationPolicies-Methode** zurückgegebene [**OIDs-Auflistung**](oids.md) mindestens ein [**OID-Objekt**](oid.md) enthält, wird das von dieser Methode zurückgegebene [**EKU-Objekt**](eku.md) ignoriert. Verwenden Sie anstelle dieser Methode die **ApplicationPolicies-Methode.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CertificateStatus**](certificatestatus.md)
</dt> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**EKU**](eku.md)
</dt> </dl>

 

 
