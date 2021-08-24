---
description: Gibt den Typ des Kryptografiedienstanbieters (Cryptographic Service Provider, CSP) an.
ms.assetid: faf2390d-bf78-4943-91f3-1db9939fedfb
title: CAPICOM_PROV_TYPE-Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROV_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bf85d2eb01ffd4290c5200e09c842f280cd5418dc5203bba068ecb5bcd65c355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879020"
---
# <a name="capicom_prov_type-enumeration"></a>CAPICOM \_ PROV \_ TYPE-Enumeration

Die **CAPICOM \_ PROV \_ TYPE-Enumeration** gibt den Typ des [*Kryptografiedienstanbieters (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) an.

## <a name="members"></a>Member



| Member                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                        | Wert |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ PROV \_ RSA \_ FULL**       | Der vollständige [*RSA-CSP.*](../secgloss/r-gly.md) Dieser Anbietertyp unterstützt sowohl [*digitale Signaturen*](../secgloss/d-gly.md) als auch die [*Datenverschlüsselung.*](../secgloss/e-gly.md)<br/>                                                            | 1     |
| **CAPICOM \_ PROV \_ RSA \_ SIG**        | Die Teilmenge des RSA-CSP, die nur die Funktionen und Algorithmen unterstützt, die für Hashes und digitale Signaturen erforderlich sind.<br/>                                                                                                                                                                                                                                        | 2     |
| **CAPICOM \_ PROV \_ DSS**             | Der [*DSS-CSP (Digital Signature Standard).*](../secgloss/d-gly.md) Dieser Anbietertyp unterstützt nur Hashes und digitale Signaturen. DSS verwendet den [*Digital Signature Algorithm*](../secgloss/d-gly.md) (DSA).<br/> | 3     |
| **CAPICOM \_ PROV \_ FORTEZZA**        | Der CSP, der die kryptografischen Protokolle und Algorithmen des [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) enthält.<br/>                                                                                      | 4     |
| **CAPICOM \_ PROV \_ MS \_ EXCHANGE**    | Der CSP, der für die kryptografischen Anforderungen von Exchange und anderen Anwendungen konzipiert wurde, die mit Microsoft Mail kompatibel sind.<br/>                                                                                                                                                                                                                                       | 5     |
| **CAPICOM \_ PROV \_ SSL**             | Der CSP, der das [*ssl-Protokoll (Secure Sockets Layer)*](../secgloss/s-gly.md) unterstützt.<br/>                                                                                                                                                                                              | 6     |
| **CAPICOM \_ PROV \_ RSA \_ SCHANNEL**   | Der CSP, der sowohl [*RSA-*](../secgloss/r-gly.md) als auch [*Schannel-Protokolle*](../secgloss/s-gly.md) unterstützt.<br/>                                                                                                                                                                                        | 12    |
| **CAPICOM \_ PROV \_ DSS \_ DH**         | Der CSP, der sowohl DSS- als auch [*Diffie-Hellman-Protokolle*](../secgloss/d-gly.md) unterstützt.<br/>                                                                                                                                                                                                          | 13    |
| **CAPICOM \_ PROV \_ EC \_ ECDSA \_ SIG**  | Der CSP, der die ECDSA-Funktionen (Elliptic Curve Digital Signature Algorithm) und algorithmen unterstützt, die für digitale Signaturen erforderlich sind.<br/>                                                                                                                                                                                                                                  | 14    |
| **CAPICOM \_ PROV \_ EC \_ ECNRA \_ SIG**  | Der CSP, der die ECNRA-Funktionen (Elliptic Curve Nyberg-Rueppel Analog) und Algorithmen unterstützt, die für digitale Signaturen erforderlich sind.<br/>                                                                                                                                                                                                                                        | 15    |
| **CAPICOM \_ PROV \_ EC \_ ECDSA \_ FULL** | Der CSP, der das vollständige ECDSA unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                   | 16    |
| **CAPICOM \_ PROV \_ EC \_ ECNRA \_ FULL** | Der CSP, der die vollständige ECNRA unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                   | 17    |
| **CAPICOM \_ PROV \_ DH \_ SCHANNEL**    | Der CSP, der sowohl [*Diffie-Hellman-*](../secgloss/d-gly.md) als [*auch Schannel-Protokolle*](../secgloss/s-gly.md) unterstützt.<br/>                                                                                                                                   | 18    |
| **CAPICOM \_ PROV \_ SPYRUS \_ LYNKS**   | Der CSP, der das SPYRUS LYNKS-Kartengerät unterstützt.<br/>                                                                                                                                                                                                                                                                                                                     | 20    |
| **CAPICOM \_ PROV \_ RNG**             | Der CSP, der die Zufallszahlengenerierung verarbeitet.<br/>                                                                                                                                                                                                                                                                                                                          | 21    |
| **CAPICOM \_ PROV \_ INTEL \_ SEC**      | Der CSP, der Intel-Sicherheit bietet.<br/>                                                                                                                                                                                                                                                                                                                                   | 22    |
| **CAPICOM \_ PROV \_ REPLACE \_ OWF**    | Der CSP, der die Ersetzung der Art und Weise unterstützt, in der aus Kennwörtern one-way-Formate generiert werden.<br/>                                                                                                                                                                                                                                                                  | 23    |
| **CAPICOM \_ PROV \_ RSA \_ AES**        | Der CSP, der sowohl digitale Signaturen als auch die Datenverschlüsselung mithilfe des [*AES-Algorithmus*](../secgloss/a-gly.md)(Advanced Encryption Standard) unterstützt.<br/>                                                                                                                                                                                       | 24    |



## <a name="remarks"></a>Hinweise

Die **CAPICOM \_ PROV \_ TYPE-Enumeration** wird von den folgenden Methoden und Eigenschaften verwendet:

-   [**PrivateKey.ProviderType-Eigenschaft.**](privatekey-providertype.md)
-   [**PrivateKey.Open-Methode.**](privatekey-open.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
