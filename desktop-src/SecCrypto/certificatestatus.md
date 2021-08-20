---
description: Enthält Informationen zum Erstellen einer Zertifikatvertrauenskette.
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: CertificateStatus-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c0c228a06da9d0a4dd93491908af0c0a2d0693125be57b675ca64e10378f253
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769999"
---
# <a name="certificatestatus-object"></a>CertificateStatus-Objekt

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Das **CertificateStatus-Objekt** enthält Informationen zum Erstellen einer Zertifikatvertrauenskette.

## <a name="members"></a>Member

Das **CertificateStatus-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **CertificateStatus-Objekt** verfügt über diese Methoden.



| Methode                                                               | Beschreibung                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](certificatestatus-applicationpolicies.md) | Gibt eine [**OIDs-Auflistung**](oids.md) zurück, die die Anwendungsrichtlinien-OIDs darstellt.<br/>                                           |
| [**CertificatePolicies**](certificatestatus-certificatepolicies.md) | Gibt eine [**OIDs-Auflistung**](oids.md) zurück, die die zertifikatrichtlinien-OIDs darstellt, die während der Kettenerstellung verwendet werden.<br/>                |
| [**EKU**](certificatestatus-eku.md)                                 | Gibt das [**EKU-Objekt**](eku.md) zurück, mit dem die EKU-Elemente festgelegt werden, die beim Festlegen des Gültigkeitsstatus eines Zertifikats überprüft werden sollen.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **CertificateStatus-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                        | Zugriffstyp           | Beschreibung                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zertifikate**](certificatestatus-certificates.md)<br/>               | Lesen/Schreiben<br/> | Legt die Auflistung von Zertifikaten fest, die zum Erstellen der Zertifikatkette verwendet werden können, oder ruft sie ab.<br/> **CAPICOM 2.0.0.3 und früher:** Die [**Certificates-Eigenschaft**](certificatestatus-certificates.md) wird nicht unterstützt.<br/>                    |
| [**CheckFlag**](certificatestatus-checkflag.md)<br/>                     | Lesen/Schreiben<br/> | Gültigkeitsprüfungsflag. Werte können mithilfe eines logischen **OR-Operators** verknüpft werden. Das Standardprüfflag ist [**CAPICOM \_ CHECK \_ ONLINE \_ ALL**](capicom-check-flag.md).<br/>                                                                                     |
| [**Ergebnis**](certificatestatus-result.md)<br/>                           | Schreibgeschützt<br/>  | Gibt an, ob das Zertifikat gültig ist. Die Gültigkeit des Zertifikats wird mithilfe der aktuellen Einstellung der [**CheckFlag-Eigenschaft**](certificatestatus-checkflag.md) und der Richtlinieneinstellungen des Zertifikats überprüft. Dies ist die Standardeigenschaft.<br/> |
| [**UrlRetrievalTimeout**](certificatestatus-urlretrievaltimeout.md)<br/> | Lesen/Schreiben<br/> | Legt die Zeitspanne fest, nach der eine URL als nicht erreichbar bestimmt wird, oder ruft sie ab.<br/>                                                                                                                                                                     |
| [**VerificationTime**](certificatestatus-verificationtime.md)<br/>       | Lesen/Schreiben<br/> | Legt den Zeitpunkt fest, zu dem das Zertifikat überprüft wurde, oder ruft diesen ab.<br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a>Hinweise

Das **CertificateStatus-Objekt** kann nicht erstellt werden.

Das **CertificateStatus-Objekt** wird von der [**Certificate.IsValid-Methode**](certificate-isvalid.md) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**Kette**](chain.md)
</dt> </dl>

 

 
