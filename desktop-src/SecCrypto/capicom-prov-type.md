---
description: Gibt den Typ des Kryptografiedienstanbieters (CSP) an.
ms.assetid: faf2390d-bf78-4943-91f3-1db9939fedfb
title: CAPICOM_PROV_TYPE-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: d9c701b453656a68573fe391775c5b27fdd2461a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358621"
---
# <a name="capicom_prov_type-enumeration"></a>CAPICOM \_ Prov \_ Type-Enumeration

Die **CAPICOM \_ Prov \_ Type** -Enumeration gibt den Typ des [*Kryptografiedienstanbieters*](../secgloss/c-gly.md) (CSP) an.

## <a name="members"></a>Member



| Member                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                        | Wert |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ Prov \_ RSA \_ Full**       | Der vollständige [*RSA*](../secgloss/r-gly.md) -CSP. Dieser Anbietertyp unterstützt sowohl [*digitale Signaturen*](../secgloss/d-gly.md) als auch Daten [*Verschlüsselung*](../secgloss/e-gly.md).<br/>                                                            | 1     |
| **CAPICOM \_ Prov \_ RSA \_ sig**        | Die Teilmenge des RSA-CSP, die nur die Funktionen und Algorithmen unterstützt, die für Hashes und digitale Signaturen erforderlich sind.<br/>                                                                                                                                                                                                                                        | 2     |
| **CAPICOM \_ Prov \_ DSS**             | Der DSS-CSP ( [*Digital Signature Standard*](../secgloss/d-gly.md) ). Dieser Anbietertyp unterstützt nur Hashes und digitale Signaturen. DSS verwendet den [*Digital Signature-Algorithmus*](../secgloss/d-gly.md) (DSA).<br/> | 3     |
| **CAPICOM \_ Prov \_ Fortezza**        | Der CSP, der die Kryptografieprotokolle und-Algorithmen im Besitz des [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST) enthält.<br/>                                                                                      | 4     |
| **CAPICOM \_ Prov \_ MS \_ Exchange**    | Der CSP, der für die kryptografischen Anforderungen von Exchange und anderen Anwendungen entworfen wurde, die mit Microsoft Mail kompatibel sind.<br/>                                                                                                                                                                                                                                       | 5     |
| **CAPICOM \_ Prov \_ SSL**             | Der CSP, der das [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL)-Protokoll unterstützt.<br/>                                                                                                                                                                                              | 6     |
| **CAPICOM \_ Prov \_ RSA \_ SChannel**   | Der CSP, der sowohl [*RSA*](../secgloss/r-gly.md) -als auch [*SChannel*](../secgloss/s-gly.md) -Protokolle unterstützt.<br/>                                                                                                                                                                                        | 12    |
| **CAPICOM \_ Prov \_ DSS \_ dh**         | Der CSP, der sowohl DSS-als auch [*Diffie-Hellman-*](../secgloss/d-gly.md) Protokolle unterstützt.<br/>                                                                                                                                                                                                          | 13    |
| **CAPICOM \_ Prov \_ EC \_ ECDSA \_ sig**  | Der CSP, der die ECDSA (Elliptic Curve Digital Signature Algorithmus)-Funktionen und-Algorithmen unterstützt, die für digitale Signaturen erforderlich sind.<br/>                                                                                                                                                                                                                                  | 14    |
| **CAPICOM \_ Prov \_ EC \_ ecnra \_ sig**  | Der CSP, der die ecnra-Funktionen (Elliptic Curve Nyberg-Rueppel analog) und die für digitale Signaturen erforderlichen Algorithmen unterstützt.<br/>                                                                                                                                                                                                                                        | 15    |
| **CAPICOM \_ Prov \_ EC \_ ECDSA \_ vollständig** | Der CSP, der den vollständigen ECDSA unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                   | 16    |
| **CAPICOM \_ Prov \_ EC \_ ecnra \_ Full** | Der CSP, der den vollständigen ecnra-unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                   | 17    |
| **CAPICOM \_ Prov \_ dh \_ SChannel**    | Der CSP, der sowohl [*Diffie-Hellman-*](../secgloss/d-gly.md) als auch [*SChannel*](../secgloss/s-gly.md) -Protokolle unterstützt.<br/>                                                                                                                                   | 18    |
| **CAPICOM \_ Prov \_ spyrus \_ Lynchs**   | Der CSP, der das spyrus lynert-Karten Gerät unterstützt.<br/>                                                                                                                                                                                                                                                                                                                     | 20    |
| **CAPICOM \_ Prov \_ RNG**             | Der CSP, der die Zufallszahlengenerierung verarbeitet.<br/>                                                                                                                                                                                                                                                                                                                          | 21    |
| **CAPICOM \_ Prov \_ Intel \_ sec**      | Der CSP, der Intel Security bereitstellt.<br/>                                                                                                                                                                                                                                                                                                                                   | 22    |
| **CAPICOM \_ Prov \_ Replace \_ owf**    | Der CSP, der die Ersetzung der Art und Weise unterstützt, in der unidirektionale Formate von Kenn Wörtern generiert werden.<br/>                                                                                                                                                                                                                                                                  | 23    |
| **CAPICOM \_ Prov \_ RSA \_ AES**        | Der CSP, der sowohl digitale Signaturen als auch Datenverschlüsselung unterstützt, mithilfe des-Advanced Encryption Standard ([*AES*](../secgloss/a-gly.md))-Algorithmus.<br/>                                                                                                                                                                                       | 24    |



## <a name="remarks"></a>Bemerkungen

Die **CAPICOM \_ Prov \_ Type** -Enumeration wird von den folgenden Methoden und Eigenschaften verwendet:

-   [**PrivateKey. ProviderType**](privatekey-providertype.md) -Eigenschaft.
-   [**PrivateKey. Open**](privatekey-open.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
