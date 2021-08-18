---
description: Ab Windows 10 bietet CNG Unterstützung für die folgenden benannten elliptischen Kurven (ANSI X9.62, X9.63, FIPS 186-2).
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: Benannte elliptische Kurven in CNG (bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691f1211b56abc41d622d20857653723be37681014a9bf72b91c1384c8f4b8cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908251"
---
# <a name="cng-named-elliptic-curves"></a>Benannte elliptische CNG-Kurven

Ab Windows 10 bietet CNG Unterstützung für die folgenden benannten elliptischen Kurven (ANSI X9.62, X9.63, FIPS 186-2).

<dl> <dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ECC \_ CURVE \_ 25519**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------|
| Name              | curve25519                                                  |
| Standard          | [Kurve 25519](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| Schlüsselgröße (Bit)   | 255                                                         |
| TLS-fähig       |                                                             |
| Objektbezeichner | Keine                                                        |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP160R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP160r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 160                                                                                                               |
| TLS-fähig       | Nein                                                                                                                |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.1                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP160T1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP160t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 160                                                                                                               |
| TLS-fähig       | Nein                                                                                                                |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.2                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP192R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP192r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 192                                                                                                               |
| TLS-fähig       | Nein                                                                                                                |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.3                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP192T1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP192t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 192                                                                                                               |
| TLS-fähig       | Nein                                                                                                                |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.4                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP224R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP224r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 224                                                                                                               |
| TLS-fähig       | Nein                                                                                                                |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.5                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP224T1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP224t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 224                                                                                                               |
| TLS-fähig       | Nein                                                                                                                |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.6                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP256R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP256r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 256                                                                                                               |
| TLS-fähig       | Ja                                                                                                               |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.7                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP256T1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP256t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 256                                                                                                               |
| TLS-fähig       | Nein                                                                                                                |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.8                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP320R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP320r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 320                                                                                                               |
| TLS-fähig       | Nein                                                                                                                |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.9                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP32 0T1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP320t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 320                                                                                                               |
| TLS-fähig       | Nein                                                                                                                |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.10                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP384R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP384r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 384                                                                                                               |
| TLS-fähig       | Ja                                                                                                               |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.11                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP384T1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP384t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 384                                                                                                               |
| TLS-fähig       | Nein                                                                                                                |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.12                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP512R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP512r1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 512                                                                                                               |
| TLS-fähig       | Ja                                                                                                               |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.13                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP512T1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Name              | brainpoolP512t1                                                                                                   |
| Standard          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Schlüsselgröße (Bit)   | 512                                                                                                               |
| TLS-fähig       | Nein                                                                                                                |
| Objektbezeichner | 1.3.36.3.3.2.8.1.1.14                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ ECC \_ CURVE \_ EC192WAPI**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|----------------------------------------------------------------|
| Name              | ec192wapi                                                      |
| Standard          | Chinese National Standard for Wireless LANs (GB 15629.11-2003) |
| Schlüsselgröße (Bit)   | 192                                                            |
| TLS-fähig       | Nein                                                             |
| Objektbezeichner | 1.2.156.11235.1.1.2.1                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT \_ ECC \_ CURVE \_ NISTP192**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Name              | nistP192                                                                                                                     |
| Standard          | [Empfohlene Elliptic Curves for Federal Government Use](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Schlüsselgröße (Bit)   | 192                                                                                                                          |
| TLS-fähig       | Ja                                                                                                                          |
| Objektbezeichner | 1.2.840.10045.3.1.1                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ \_ \_ ECC-KURVE NISTP224**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Name              | nistP224                                                                                                                     |
| Standard          | [Empfohlene Elliptic Curves for Federal Government Use](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Schlüsselgröße (Bit)   | 224                                                                                                                          |
| TLS-fähig       | Ja                                                                                                                          |
| Objektbezeichner | 1.3.132.0.33                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT \_ ECC \_ CURVE \_ NISTP256**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Name              | nistP256                                                                                                                     |
| Standard          | [Empfohlene Elliptic Curves for Federal Government Use](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Schlüsselgröße (Bit)   | 256                                                                                                                          |
| TLS-fähig       | Ja                                                                                                                          |
| Objektbezeichner | 1.2.840.10045.3.1.7                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ \_ \_ ECC-KURVE NISTP384**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Name              | nistP384                                                                                                                     |
| Standard          | [Empfohlene Elliptic Curves for Federal Government Use](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Schlüsselgröße (Bit)   | 384                                                                                                                          |
| TLS-fähig       | Ja                                                                                                                          |
| Objektbezeichner | 1.3.132.0.34                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT \_ ECC \_ CURVE \_ NISTP521**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Name              | nistP521                                                                                                                     |
| Standard          | [Empfohlene Elliptic Curves for Federal Government Use](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Schlüsselgröße (Bit)   | 521                                                                                                                          |
| TLS-fähig       | Ja                                                                                                                          |
| Objektbezeichner | 1.3.132.0.35                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ \_ \_ ECC-KURVE NUMSP256T1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Name              | numsP256t1                                                                                                                              |
| Standard          | [Spezifikation der Kurvenauswahl und unterstützter Kurvenparameter in MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Schlüsselgröße (Bit)   | 256                                                                                                                                     |
| TLS-fähig       | Nein                                                                                                                                      |
| Objektbezeichner | Keine                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ \_ \_ ECC-KURVE NUMSP384T1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Name              | numsP384t1                                                                                                                              |
| Standard          | [Spezifikation der Kurvenauswahl und unterstützter Kurvenparameter in MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Schlüsselgröße (Bit)   | 384                                                                                                                                     |
| TLS-fähig       | Nein                                                                                                                                      |
| Objektbezeichner | Keine                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT \_ ECC \_ CURVE \_ NUMSP512T1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Name              | numsP512t1                                                                                                                              |
| Standard          | [Spezifikation der Kurvenauswahl und unterstützter Kurvenparameter in MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Schlüsselgröße (Bit)   | 512                                                                                                                                     |
| TLS-fähig       | Nein                                                                                                                                      |
| Objektbezeichner | Keine                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ \_ECC-KURVE \_ SECP160K1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Name              | secP160k1                                                                       |
| Standard          | [Empfohlene Domänenparameter für elliptische Kurven](https://www.secg.org/sec2-v2.pdf) |
| Schlüsselgröße (Bit)   | 160                                                                             |
| TLS-fähig       | Ja                                                                             |
| Objektbezeichner | 1.3.132.0.9                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ECC-KURVE \_ SECP160R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Name              | secP160r1                                                                       |
| Standard          | [Empfohlene Domänenparameter für elliptische Kurven](https://www.secg.org/sec2-v2.pdf) |
| Schlüsselgröße (Bit)   | 160                                                                             |
| TLS-fähig       | Ja                                                                             |
| Objektbezeichner | 1.3.132.0.8                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ \_ECC-KURVE \_ SECP160R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Name              | secP160r2                                                                       |
| Standard          | [Empfohlene Domänenparameter für elliptische Kurven](https://www.secg.org/sec2-v2.pdf) |
| Schlüsselgröße (Bit)   | 160                                                                             |
| TLS-fähig       | Ja                                                                             |
| Objektbezeichner | 1.3.132.0.30                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP192K1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Name              | secP192k1                                                                       |
| Standard          | [Empfohlene Domänenparameter für elliptische Kurven](https://www.secg.org/sec2-v2.pdf) |
| Schlüsselgröße (Bit)   | 192                                                                             |
| TLS-fähig       | Ja                                                                             |
| Objektbezeichner | 1.3.132.0.31                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ \_ECC-KURVE \_ SECP192R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Name              | secP192r1                                                                       |
| Standard          | [Empfohlene Domänenparameter für elliptische Kurven](https://www.secg.org/sec2-v2.pdf) |
| Schlüsselgröße (Bit)   | 192                                                                             |
| TLS-fähig       | Ja                                                                             |
| Objektbezeichner | 1.2.840.10045.3.1.1                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP224K1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Name              | secP224k1                                                                       |
| Standard          | [Empfohlene Domänenparameter für elliptische Kurven](https://www.secg.org/sec2-v2.pdf) |
| Schlüsselgröße (Bit)   | 224                                                                             |
| TLS-fähig       | Ja                                                                             |
| Objektbezeichner | 1.3.132.0.32                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP224R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Name              | secP224r1                                                                       |
| Standard          | [Empfohlene Domänenparameter für elliptische Kurven](https://www.secg.org/sec2-v2.pdf) |
| Schlüsselgröße (Bit)   | 224                                                                             |
| TLS-fähig       | Ja                                                                             |
| Objektbezeichner | 1.3.132.0.33                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP256K1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Name              | secP256k1                                                                       |
| Standard          | [Empfohlene Domänenparameter für elliptische Kurven](https://www.secg.org/sec2-v2.pdf) |
| Schlüsselgröße (Bit)   | 256                                                                             |
| TLS-fähig       | Ja                                                                             |
| Objektbezeichner | 1.3.132.0.10                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP256R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Name              | secP256r1                                                                       |
| Standard          | [Empfohlene Domänenparameter für elliptische Kurven](https://www.secg.org/sec2-v2.pdf) |
| Schlüsselgröße (Bit)   | 256                                                                             |
| TLS-fähig       | Ja                                                                             |
| Objektbezeichner | 1.2.840.10045.3.1.7                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ \_ECC-KURVE \_ SECP384R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Name              | secP384r1                                                                       |
| Standard          | [Empfohlene Domänenparameter für elliptische Kurven](https://www.secg.org/sec2-v2.pdf) |
| Schlüsselgröße (Bit)   | 384                                                                             |
| TLS-fähig       | Ja                                                                             |
| Objektbezeichner | 1.3.132.0.34                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP521R1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------|
| Name              | secP521r1                                                                       |
| Standard          | [Empfohlene Domänenparameter für elliptische Kurven](https://www.secg.org/sec2-v2.pdf) |
| Schlüsselgröße (Bit)   | 521                                                                             |
| TLS-fähig       | Ja                                                                             |
| Objektbezeichner | 1.3.132.0.35                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT \_ ECC \_ CURVE \_ WTLS12**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|--------------|
| Name              | wtls12       |
| Standard          | WTLS         |
| Schlüsselgröße (Bit)   | 224          |
| TLS-fähig       | Nein           |
| Objektbezeichner | 1.3.132.0.33 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT \_ ECC \_ CURVE \_ WTLS7**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|--------------|
| Name              | wtls7        |
| Standard          | WTLS         |
| Schlüsselgröße (Bit)   | 160          |
| TLS-fähig       | Nein           |
| Objektbezeichner | 1.3.132.0.30 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ \_ECC-KURVE \_ WTLS9**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------|
| Name              | wtls9         |
| Standard          | WTLS          |
| Schlüsselgröße (Bit)   | 160           |
| TLS-fähig       | Nein            |
| Objektbezeichner | 2.23.43.1.4.9 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P192V1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------|
| Name              | x962P192v1          |
| Standard          | ANSI X9.62          |
| Schlüsselgröße (Bit)   | 192                 |
| TLS-fähig       | Nein                  |
| Objektbezeichner | 1.2.840.10045.3.1.1 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P192V2**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------|
| Name              | x962P192v2          |
| Standard          | ANSI X9.62          |
| Schlüsselgröße (Bit)   | 192                 |
| TLS-fähig       | Nein                  |
| Objektbezeichner | 1.2.840.10045.3.1.2 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P192V3**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------|
| Name              | x962P192v3          |
| Standard          | ANSI X9.62          |
| Schlüsselgröße (Bit)   | 192                 |
| TLS-fähig       | Nein                  |
| Objektbezeichner | 1.2.840.10045.3.1.3 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P239V1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------|
| Name              | x962P239v1          |
| Standard          | ANSI X9.62          |
| Schlüsselgröße (Bit)   | 239                 |
| TLS-fähig       | Nein                  |
| Objektbezeichner | 1.2.840.10045.3.1.4 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P239V2**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------|
| Name              | x962P239v2          |
| Standard          | ANSI X9.62          |
| Schlüsselgröße (Bit)   | 239                 |
| TLS-fähig       | Nein                  |
| Objektbezeichner | 1.2.840.10045.3.1.5 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P239V3**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------|
| Name              | x962P239v3          |
| Standard          | ANSI X9.62          |
| Schlüsselgröße (Bit)   | 239                 |
| TLS-fähig       | Nein                  |
| Objektbezeichner | 1.2.840.10045.3.1.6 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P256V1**</dt> <dd> <dl> <dt> 

| Anforderung | Wert |
|-------------------|---------------------|
| Name              | x962P256v1          |
| Standard          | ANSI X9.62          |
| Schlüsselgröße (Bit)   | 256                 |
| TLS-fähig       | Nein                  |
| Objektbezeichner | 1.2.840.10045.3.1.7 |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Um eine benannte Kurve zu verwenden, rufen Sie [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) auf, indem Sie entweder den **BCRYPT \_ ECDSA \_ ALGORITHM** oder den **BCRYPT \_ ECDH \_ ALGORITHM** als Algorithmus-ID verwenden. Rufen Sie dann [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) auf, und legen Sie die **BCRYPT \_ ECC CURVE \_ \_ NAME-Eigenschaft** auf eine der oben genannten Kurven oder eine beliebige benannte Kurven fest, die auf dem Computer registriert sind, wie im `certutil -displayEccCurve` Befehl gezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Bcrypt.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




