---
description: Stellt die Namen für CAPICOM-Objektbezeichner bereit.
ms.assetid: 6c1eb2cc-84ac-4920-99ba-56ac8de4a851
title: CAPICOM_OID-Enumeration (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_OID
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8c008a77e11bd7803dfb09ed2e6ddf1f57ed8695f2de33655239eb73ac49a248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879030"
---
# <a name="capicom_oid-enumeration"></a>\_CAPICOM-OID-Enumeration

Die **\_ CAPICOM-OID-Enumeration** stellt die Namen für CAPICOM-Objektbezeichner bereit.

Diese Enumeration wird von der [**OID verwendet. Name-Eigenschaft.**](oid-name.md)

## <a name="members"></a>Member



| Member                                                        | BESCHREIBUNG                                                                                                                                                                                                                                    | Wert |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ OID \_ OTHER**                                       | Das -Objekt ist keiner der vordefinierten CAPICOM-Objekttypen.<br/>                                                                                                                                                                       | 0     |
| **CAPICOM \_ OID \_ AUTHORITY \_ KEY \_ IDENTIFIER \_ EXTENSION**       | Das -Objekt ist eine Zertifikaterweiterung, die den Bezeichner des öffentlichen Schlüssels der Zertifizierungsstelle enthält.<br/>                                                                                                                  | 1     |
| **ERWEITERUNG FÜR \_ CAPICOM-OIDSCHLÜSSELATTRIBUTE \_ \_ \_**                  | Das -Objekt ist eine Zertifikaterweiterung, die optionale Attribute eines öffentlichen Schlüssels enthält.<br/>                                                                                                                                            | 2     |
| **CAPICOM \_ OID \_ CERT \_ POLICIES \_ 95 \_ EXTENSION**               | Das -Objekt ist eine Zertifikaterweiterung, die Windows 95-Zertifikatrichtlinieninformationen enthält.<br/>                                                                                                                                      | 3     |
| **\_EINSCHRÄNKUNGSERWEITERUNG FÜR CAPICOM-OIDSCHLÜSSELVERWENDUNG \_ \_ \_ \_**          | Das -Objekt ist eine Zertifikaterweiterung, die Einschränkungen für die Verwendung des öffentlichen Schlüssels eines Zertifikats enthält.<br/>                                                                                                                          | 4     |
| **CAPICOM \_ OID \_ LEGACY \_ POLICY \_ MAPPINGS \_ EXTENSION**         | Das -Objekt ist eine Zertifikaterweiterung, die Legacy-Richtlinienzuordnungsinformationen enthält.<br/>                                                                                                                                              | 5     |
| **CAPICOM \_ OID \_ SUBJECT \_ ALT \_ NAME \_ EXTENSION**               | Das -Objekt ist eine Zertifikaterweiterung, die einen alternativen Namen für den Antragsteller des Zertifikats enthält.<br/>                                                                                                                         | 6     |
| **CAPICOM \_ OID \_ ISSUER \_ ALT \_ NAME \_ EXTENSION**                | Das -Objekt ist eine Zertifikaterweiterung, die einen alternativen Namen für den Aussteller des Zertifikats enthält.<br/>                                                                                                                          | 7     |
| **CAPICOM \_ OID \_ BASIC \_ CONSTRAINTS \_ EXTENSION**               | Das -Objekt ist eine Zertifikaterweiterung, die angibt, ob der zertifizierte Antragsteller als Zertifizierungsstelle, Als Endentität oder beides fungieren kann. <br/>                                                                                                        | 8     |
| **ERWEITERUNG FÜR \_ CAPICOM-OID-ANTRAGSTELLERSCHLÜSSELBEZEICHNER \_ \_ \_ \_**         | Das -Objekt ist eine Zertifikaterweiterung, die den Schlüsselbezeichner des Antragstellers des Zertifikats enthält.<br/>                                                                                                                           | 9     |
| **\_ \_ \_ CAPICOM-OIDSCHLÜSSELVERWENDUNGSERWEITERUNG \_**                       | Das -Objekt ist eine Zertifikaterweiterung, die Informationen zur beabsichtigten Verwendung des öffentlichen Schlüssels eines Zertifikats enthält.<br/>                                                                                                               | 10    |
| **CAPICOM \_ OID \_ PRIVATEKEY \_ USAGE \_ PERIOD \_ EXTENSION**        | Das -Objekt ist eine Zertifikaterweiterung, die Informationen zum Zeitraum enthält, in dem der private Schlüssel eines Zertifikats verwendet werden kann.<br/>                                                                                           | 11    |
| **CAPICOM \_ OID \_ SUBJECT \_ ALT \_ NAME2 \_ EXTENSION**              | Das -Objekt ist eine Zertifikaterweiterung, die einen alternativen Namen für den Antragsteller des Zertifikats enthält.<br/>                                                                                                                         | 12    |
| **CAPICOM \_ OID \_ ISSUER \_ ALT \_ NAME2 \_ EXTENSION**               | Das -Objekt ist eine Zertifikaterweiterung, die einen alternativen Namen für den Aussteller des Zertifikats enthält.<br/>                                                                                                                          | 13    |
| **CAPICOM \_ OID \_ BASIC \_ CONSTRAINTS2 \_ EXTENSION**              | Das -Objekt ist eine Zertifikaterweiterung, die angibt, ob der zertifizierte Antragsteller als Zertifizierungsstelle, Als Endentität oder beides fungieren kann. <br/>                                                                                                        | 14    |
| **ERWEITERUNG FÜR \_ CAPICOM-OIDNAMENEINSCHRÄNKUNGEN \_ \_ \_**                | Das -Objekt ist eine Zertifikaterweiterung, die Informationen zu Zertifikaten enthält, die ausdrücklich zugelassen oder von der Vertrauenswürdigkeit ausgeschlossen sind.<br/>                                                                                          | 15    |
| **CAPICOM \_ OID \_ CRL \_ DIST \_ POINTS \_ EXTENSION**                | Das -Objekt ist eine Zertifikaterweiterung, die Informationen enthält, die zum Aktualisieren der Zertifikatsperrliste (Certificate Revocation List, CRL) verwendet werden.<br/>                                                                                                               | 16    |
| **CAPICOM \_ OID \_ CERT \_ POLICIES \_ EXTENSION**                   | Das -Objekt ist eine Zertifikaterweiterung, die eine Liste der Richtlinien enthält, die das Zertifikat unterstützt.<br/>                                                                                                                           | 17    |
| **CAPICOM \_ OID \_ POLICY \_ MAPPINGS \_ EXTENSION**                 | Das -Objekt ist eine Zertifikaterweiterung, die Zuordnungen zwischen Richtlinien in verschiedenen Domänen bereitstellt.<br/>                                                                                                                                 | 18    |
| **CAPICOM \_ OID \_ AUTHORITY \_ KEY \_ IDENTIFIER2 \_ EXTENSION**      | Das -Objekt ist eine Zertifikaterweiterung, die den Bezeichner des öffentlichen Schlüssels der Zertifizierungsstelle enthält.<br/>                                                                                                                                            | 19    |
| **ERWEITERUNG FÜR \_ CAPICOM-OIDRICHTLINIENEINSCHRÄNKUNGEN \_ \_ \_**              | Das -Objekt ist eine Zertifikaterweiterung, die eingerichtete Richtlinien zum Akzeptieren von Zertifikaten als vertrauenswürdig enthält.<br/>                                                                                                                     | 20    |
| **\_ \_ \_ ERWEITERTE \_ SCHLÜSSELVERWENDUNGSERWEITERUNG \_ FÜR CAPICOM-OID**             | Das -Objekt ist eine Zertifikaterweiterung, die erweiterte Informationen zur beabsichtigten Verwendung des öffentlichen Schlüssels eines Zertifikats enthält.<br/>                                                                                                      | 21    |
| **\_ \_ \_ CAPICOM-OID-ZERTIFIKATVORLAGENERWEITERUNG \_**            | Das -Objekt ist eine Zertifikaterweiterung, die eine Zertifikatvorlage enthält.<br/>                                                                                                                                                         | 22    |
| **CAPICOM \_ OID \_ APPLICATION \_ CERT \_ POLICIES \_ EXTENSION**      | Das -Objekt ist eine Zertifikaterweiterung, die die Anwendungsrichtlinie des Zertifikats enthält.<br/>                                                                                                                                      | 23    |
| **ERWEITERUNG FÜR \_ CAPICOM-OIDANWENDUNGSRICHTLINIENZUORDNUNGEN \_ \_ \_ \_**    | Das -Objekt ist eine Zertifikaterweiterung, die Zuordnungen zwischen verschiedenen Anwendungsrichtlinien enthält.<br/>                                                                                                                                | 24    |
| **ERWEITERUNG FÜR \_ CAPICOM-OIDANWENDUNGSRICHTLINIENEINSCHRÄNKUNGEN \_ \_ \_ \_** | Das -Objekt ist eine Zertifikaterweiterung, die die Anwendungsrichtlinieneinschränkungen des Zertifikats enthält.<br/>                                                                                                                          | 25    |
| **ZUGRIFFSERWEITERUNG FÜR \_ CAPICOM-OID-AUTORITÄTSINFORMATIONEN \_ \_ \_ \_**          | Das -Objekt ist eine Zertifikaterweiterung, die angibt, wie auf Informationen und Dienste der Zertifizierungsstelle für den Zertifikataussteller zugegriffen werden soll.<br/>                                                                                                   | 26    |
| **CAPICOM \_ OID \_ SERVER \_ AUTH \_ EKU**                           | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat zum Authentifizieren eines Servers verwendet werden kann.<br/>                                                                                                                | 100   |
| **CAPICOM \_ OID \_ CLIENT \_ AUTH \_ EKU**                           | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat zum Authentifizieren eines Clients verwendet werden kann.<br/>                                                                                                                | 101   |
| **\_ \_ \_ \_ CAPICOM-OID-CODESIGNATUR-EKU**                          | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat zum Erstellen einer digitalen Signatur verwendet werden kann.<br/>                                                                                                           | 102   |
| **\_ \_ \_ E-MAIL-SCHUTZ-E-KU FÜR CAPICOM-OID \_**                      | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für den E-Mail-Schutz verwendet werden kann.<br/>                                                                                                                    | 103   |
| **\_CAPICOM-OID \_ \_ IPSEC-ENDSYSTEM-EKU \_ \_**                     | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für ein IPsec-Endsystem verwendet werden kann.<br/>                                                                                                                 | 104   |
| **\_CAPICOM-OID \_ \_ IPSEC-TUNNEL-EKU \_**                          | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für IPsec-Tunneling verwendet werden kann.<br/>                                                                                                                     | 105   |
| **\_CAPICOM-OID \_ \_ IPSEC-BENUTZER-EKU \_**                            | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für einen IPsec-Benutzer verwendet werden kann.<br/>                                                                                                                       | 106   |
| **CAPICOM \_ OID \_ TIME \_ STAMPING \_ EKU**                         | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für den Zeitstempel verwendet werden kann.<br/>                                                                                                                       | 107   |
| **CAPICOM \_ OID \_ CTL \_ USAGE \_ SIGNING \_ EKU**                    | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat zum Signieren der Zertifikatvertrauensliste (Certificate Trust List, CTL) verwendet werden kann.<br/>                                                                                                | 108   |
| **\_CAPICOM-OID: \_ \_ ZEITSTEMPELSIGNATUR-EKU \_ \_**                   | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat zum Signieren eines Zeitstempels verwendet werden kann.<br/>                                                                                                                    | 109   |
| **CAPICOM \_ OID \_ SERVER \_ GATED \_ CRYPTO \_ EKU**                  | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für die servergegatete Kryptografie (Server [*Gated Cryptography,*](../secgloss/s-gly.md) SGC) verwendet werden kann.<br/> | 110   |
| **\_CAPICOM-OID: \_ VERSCHLÜSSELNDE \_ \_ \_ DATEISYSTEM-EKU**               | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für die verschlüsselndes Dateisystem (EFS) verwendet werden kann. [](../secgloss/e-gly.md)<br/>      | 111   |
| **CAPICOM \_ OID \_ EFS \_ RECOVERY \_ EKU**                          | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für die Wiederherstellung des EFS verwendet werden kann.<br/>                                                                                                                 | 112   |
| **CAPICOM \_ OID \_ WHQL \_ CRYPTO \_ EKU**                           | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für Windows WHQL-Kryptografie (Hardware Quality Labs) verwendet werden kann.<br/>                                                                                   | 113   |
| **\_CAPICOM-OID \_ NT5 \_ CRYPTO \_ EKU**                            | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für die Windows Server 2003- und Windows XP-Kryptografie verwendet werden kann.<br/>                                                                                     | 114   |
| **CAPICOM \_ OID \_ OEM \_ WHQL \_ CRYPTO \_ EKU**                      | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für oem-WHQL-Kryptografie (Original Equipment Manufacturers) verwendet werden kann.<br/>                                                                            | 115   |
| **CAPICOM \_ OID \_ EMBED \_ NT CRYPTO \_ \_ EKU**                    | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für Windows NT Embedded-Kryptografie verwendet werden kann.<br/>                                                                                                    | 116   |
| **CAPICOM \_ OID \_ ROOT \_ LIST \_ SIGNER \_ EKU**                     | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat zum Signieren einer Stammliste verwendet werden kann.<br/>                                                                                                                     | 117   |
| **CAPICOM \_ OID \_ QUALIFIED \_ SUBORDINATION \_ EKU**               | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für die qualifizierte Unterordnung verwendet werden kann.<br/>                                                                                                             | 118   |
| **\_ \_ \_ CAPICOM-OID-SCHLÜSSELWIEDERHERSTELLUNGS-EKU \_**                          | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für die Schlüsselwiederherstellung verwendet werden kann.<br/>                                                                                                                        | 119   |
| **CAPICOM \_ OID \_ DIGITAL \_ RIGHTS \_ EKU**                        | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für digitale Rechte verwendet werden kann.<br/>                                                                                                                      | 120   |
| **CAPICOM \_ OID \_ LICENSES \_ EKU**                               | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für Lizenzen verwendet werden kann.<br/>                                                                                                                            | 121   |
| **\_ \_ \_ CAPICOM-OID-LIZENZSERVER-EKU \_**                        | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für einen Lizenzserver verwendet werden kann.<br/>                                                                                                                    | 122   |
| **\_CAPICOM-OID \_ \_ \_ SMARTCARD-ANMELDE-EKU \_**                     | Das -Objekt ist ein [**EKU-Objekt,**](eku.md) das angibt, dass das Zertifikat für die Smartcardanmeldung verwendet werden kann.<br/>                                                                                                                    | 123   |
| **CAPICOM \_ OID \_ PKIX \_ POLICY \_ QUALIFIER \_ CPS**                | Das -Objekt ist eine Certification Practice Statement (CPS), die für den PIX-Richtlinienqualifizierer (Public Key Infrastructure X.509) verwendet werden kann.<br/>                                                                                            | 124   |
| **CAPICOM \_ OID \_ PKIX \_ POLICY \_ QUALIFIER \_ USERNOTICE**         | Das -Objekt ist ein Benutzerhinweis, der für den PIX-Richtlinienqualifizierer (Public Key Infrastructure X.509) verwendet werden kann.<br/>                                                                                                                       | 125   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
