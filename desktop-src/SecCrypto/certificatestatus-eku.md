---
description: Gibt das EKU-Objekt zurück, das zum Erstellen des Ketten Objekts verwendet wird.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: CertificateStatus. EKU-Methode
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
ms.openlocfilehash: d386251c6d7f674d3850de275559bcb87ea6d61e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369951"
---
# <a name="certificatestatuseku-method"></a>CertificateStatus. EKU-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Die **EKU** -Methode gibt das [**EKU**](eku.md) -Objekt zurück, das zum Erstellen des [**Ketten**](chain.md) Objekts verwendet wird.

## <a name="syntax"></a>Syntax


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein [**EKU**](eku.md) -Objekt zurück, das die erweiterte Schlüssel Verwendung des [*Zertifikats*](../secgloss/c-gly.md)angibt. Mit der EKU-Einstellung wird die gültige Verwendung eines Zertifikats festgelegt. Für jedes Zertifikat kann nur ein einzelnes **EKU** -Objekt festgelegt werden.

## <a name="remarks"></a>Bemerkungen

Die [**CertificateStatus. applicationpolicies**](certificatestatus-applicationpolicies.md) -Methode bietet die gleiche Funktionalität wie diese Methode, ermöglicht jedoch, dass viele Einstellungen anstelle von nur einer angegeben werden. Wenn die von der **applicationpolicies** -Methode zurückgegebene [**OIDs**](oids.md) -Auflistung ein oder mehrere [**OID**](oid.md) -Objekte enthält, wird das von dieser Methode zurückgegebene [**EKU**](eku.md) -Objekt ignoriert. Verwenden Sie die **applicationpolicies** -Methode anstelle dieser Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CertificateStatus**](certificatestatus.md)
</dt> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**EKU**](eku.md)
</dt> </dl>

 

 
