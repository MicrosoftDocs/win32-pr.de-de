---
description: Enthält Informationen zum Erstellen einer Zertifikats Vertrauenskette.
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
ms.openlocfilehash: e9a6cb31a00f4d2943e68670930e6cbc4436b6b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371044"
---
# <a name="certificatestatus-object"></a>CertificateStatus-Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509ChainStatus-Struktur**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **CertificateStatus** -Objekt enthält Informationen zum Erstellen einer Zertifikats Vertrauenskette.

## <a name="members"></a>Member

Das **CertificateStatus** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **CertificateStatus** -Objekt verfügt über diese Methoden.



| Methode                                                               | BESCHREIBUNG                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Applicationpolicies**](certificatestatus-applicationpolicies.md) | Gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die OIDs der Anwendungs Richtlinie darstellt.<br/>                                           |
| [**Certificatepolicies**](certificatestatus-certificatepolicies.md) | Gibt eine [**OIDs**](oids.md) -Auflistung zurück, die die während der Ketten Bildung verwendeten Zertifikat Richtlinien-OIDs darstellt.<br/>                |
| [**EKU**](certificatestatus-eku.md)                                 | Gibt das [**EKU**](eku.md) -Objekt zurück, mit dem die EKU-Elemente festgelegt werden, die beim Einrichten des Gültigkeits Status eines Zertifikats überprüft werden.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **CertificateStatus** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                        | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zertifikate**](certificatestatus-certificates.md)<br/>               | Lesen/Schreiben<br/> | Legt die Auflistung der Zertifikate fest, die zum Erstellen der Zertifikat Kette verwendet werden können, oder ruft diese ab.<br/> **CAPICOM 2.0.0.3 und früher:** Die Eigenschaft [**Zertifikate**](certificatestatus-certificates.md) wird nicht unterstützt.<br/>                    |
| [**Checkflag**](certificatestatus-checkflag.md)<br/>                     | Lesen/Schreiben<br/> | Flag zum Überprüfen der Gültigkeit. Werte können mithilfe eines logischen **or** -Operators verknüpft werden. Das Standardflag für die Überprüfung lautet [**CAPICOM \_ \_ Online \_ alle überprüfen**](capicom-check-flag.md).<br/>                                                                                     |
| [**Dadurch**](certificatestatus-result.md)<br/>                           | Schreibgeschützt<br/>  | Gibt an, ob das Zertifikat gültig ist. Die Gültigkeit des Zertifikats wird mithilfe der aktuellen Einstellung der Eigenschaft [**checkflag**](certificatestatus-checkflag.md) und den Richtlinien Einstellungen des Zertifikats überprüft. Dies ist die Standard Eigenschaft.<br/> |
| [**UrlRetrievalTimeout**](certificatestatus-urlretrievaltimeout.md)<br/> | Lesen/Schreiben<br/> | Legt die Zeitspanne fest, nach der eine URL als nicht erreichbar festgelegt wird, oder ruft Sie ab.<br/>                                                                                                                                                                     |
| [**VerificationTime**](certificatestatus-verificationtime.md)<br/>       | Lesen/Schreiben<br/> | Legt die Uhrzeit fest, zu der das Zertifikat überprüft wurde, oder ruft diese ab.<br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Das **CertificateStatus** -Objekt kann nicht erstellt werden.

Das **CertificateStatus** -Objekt wird von der [**Certificate. IsValid**](certificate-isvalid.md) -Methode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> <dt>

[**Ketten**](chain.md)
</dt> </dl>

 

 
