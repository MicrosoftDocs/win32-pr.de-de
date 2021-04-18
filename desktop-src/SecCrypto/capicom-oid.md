---
description: Stellt die Namen für CAPICOM-Objekt Bezeichner bereit.
ms.assetid: 6c1eb2cc-84ac-4920-99ba-56ac8de4a851
title: CAPICOM_OID-Enumeration (CAPICOM. h)
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
ms.openlocfilehash: 4cedd7c039212b7bae3e681d7e0d594d3e1b8de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358041"
---
# <a name="capicom_oid-enumeration"></a>CAPICOM- \_ OID-Enumeration

Die **CAPICOM- \_ OID** -Enumeration stellt die Namen für CAPICOM-Objekt Bezeichner bereit.

Diese Enumeration wird von der [**OID verwendet. Name**](oid-name.md) -Eigenschaft.

## <a name="members"></a>Member



| Member                                                        | BESCHREIBUNG                                                                                                                                                                                                                                    | Wert |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **andere CAPICOM \_ OID \_**                                       | Das-Objekt ist keiner der vordefinierten CAPICOM-Objekttypen.<br/>                                                                                                                                                                       | 0     |
| **\_ \_ \_ \_ schlüsselbezeichnererweiterung der CAPICOM-OID-Autorität \_**       | Bei dem Objekt handelt es sich um eine Zertifikat Erweiterung, die den öffentlichen Schlüssel Bezeichner der Zertifizierungsstelle (Certification Authority, ca) enthält.<br/>                                                                                                                  | 1     |
| **Erweiterung für CAPICOM- \_ OID- \_ Schlüssel \_ Attribute \_**                  | Das-Objekt ist eine Zertifikat Erweiterung, die optionale Attribute eines öffentlichen Schlüssels enthält.<br/>                                                                                                                                            | 2     |
| **CAPICOM \_ OID \_ CERT \_ Policies \_ 95- \_ Erweiterung**               | Das-Objekt ist eine Zertifikat Erweiterung, die Informationen zu Windows 95-Zertifikat Richtlinien enthält.<br/>                                                                                                                                      | 3     |
| **Erweiterung für die Verwendung von CAPICOM \_ OID \_ Key \_ \_ \_**          | Das-Objekt ist eine Zertifikat Erweiterung, die Einschränkungen bezüglich der Verwendung des öffentlichen Schlüssels eines Zertifikats enthält.<br/>                                                                                                                          | 4     |
| **Erweiterung der Vorgänger Richtlinien Zuordnungen für CAPICOM \_ OID \_ \_ \_ \_**         | Bei dem Objekt handelt es sich um eine Zertifikat Erweiterung, die Legacy Informationen zur Richtlinien Zuordnung enthält.<br/>                                                                                                                                              | 5     |
| **Erweiterung des CAPICOM \_ OID- \_ Subject-alt- \_ \_ namens \_**               | Das-Objekt ist eine Zertifikat Erweiterung, die einen alternativen Namen für den Betreff des Zertifikats enthält.<br/>                                                                                                                         | 6     |
| **Erweiterung des CAPICOM \_ OID- \_ Aussteller-alt- \_ \_ namens \_**                | Das-Objekt ist eine Zertifikat Erweiterung, die einen alternativen Namen für den Aussteller des Zertifikats enthält.<br/>                                                                                                                          | 7     |
| **Erweiterung für CAPICOM \_ OID \_ Basic- \_ Einschränkungen \_**               | Das-Objekt ist eine Zertifikat Erweiterung, die angibt, ob der zertifizierte Betreff als Zertifizierungsstelle, als Endentität oder beides fungieren kann. <br/>                                                                                                        | 8     |
| **Erweiterung des CAPICOM \_ OID- \_ Subject \_ Key \_ Identifier \_**         | Das-Objekt ist eine Zertifikat Erweiterung, die den Schlüssel Bezeichner des Antragstellers des Zertifikats enthält.<br/>                                                                                                                           | 9     |
| **Erweiterung "CAPICOM \_ OID \_ Key \_ Usage \_ "**                       | Das-Objekt ist eine Zertifikat Erweiterung, die Informationen über die beabsichtigte Verwendung des öffentlichen Schlüssels eines Zertifikats enthält.<br/>                                                                                                               | 10    |
| **CAPICOM \_ OID \_ PrivateKey- \_ Verwendungs \_ Zeit \_ Erweiterung**        | Das-Objekt ist eine Zertifikat Erweiterung, die Informationen über den Zeitraum enthält, in dem der private Schlüssel eines Zertifikats verwendet werden kann.<br/>                                                                                           | 11    |
| **CAPICOM \_ OID \_ Subject \_ alt \_ name2 \_ Erweiterung**              | Das-Objekt ist eine Zertifikat Erweiterung, die einen alternativen Namen für den Betreff des Zertifikats enthält.<br/>                                                                                                                         | 12    |
| **CAPICOM \_ OID- \_ Aussteller \_ alt \_ name2 \_ Erweiterung**               | Das-Objekt ist eine Zertifikat Erweiterung, die einen alternativen Namen für den Aussteller des Zertifikats enthält.<br/>                                                                                                                          | 13    |
| **CAPICOM \_ OID \_ Basic \_ CONSTRAINTS2 \_ Erweiterung**              | Das-Objekt ist eine Zertifikat Erweiterung, die angibt, ob der zertifizierte Betreff als Zertifizierungsstelle, als Endentität oder beides fungieren kann. <br/>                                                                                                        | 14    |
| **Erweiterung für "CAPICOM \_ OID \_ Name \_ Einschränkungs" \_**                | Bei dem Objekt handelt es sich um eine Zertifikat Erweiterung, die Informationen zu Zertifikaten enthält, die von der Vertrauensstellung ausdrücklich zugelassen oder ausgeschlossen sind.<br/>                                                                                          | 15    |
| **Erweiterung für CAPICOM \_ OID \_ CRL \_ dist \_ Points \_**                | Bei dem Objekt handelt es sich um eine Zertifikat Erweiterung, die Informationen enthält, die zum Aktualisieren der Zertifikat Sperr Liste (CRL) verwendet werden.<br/>                                                                                                               | 16    |
| **Erweiterung für CAPICOM- \_ OID- \_ Zertifikat \_ Richtlinien \_**                   | Das-Objekt ist eine Zertifikat Erweiterung, die eine Liste der Richtlinien enthält, die das Zertifikat unterstützt.<br/>                                                                                                                           | 17    |
| **Erweiterung für CAPICOM-OID-Richtlinien Zuordnungen \_ \_ \_ \_**                 | Das-Objekt ist eine Zertifikat Erweiterung, die Zuordnungen zwischen Richtlinien in verschiedenen Domänen bereitstellt.<br/>                                                                                                                                 | 18    |
| **CAPICOM \_ OID \_ Authority \_ Key \_ Bezeichner2 \_ Erweiterung**      | Das-Objekt ist eine Zertifikat Erweiterung, die den öffentlichen Schlüssel Bezeichner der Zertifizierungsstelle enthält.<br/>                                                                                                                                            | 19    |
| **Erweiterung für CAPICOM- \_ OID- \_ Richtlinien \_ Einschränkungen \_**              | Das-Objekt ist eine Zertifikat Erweiterung, die festgelegte Richtlinien für die Annahme von Zertifikaten als vertrauenswürdig enthält.<br/>                                                                                                                     | 20    |
| **Erweiterung "CAPICOM \_ OID \_ Enhanced \_ Key \_ Usage \_ "**             | Das-Objekt ist eine Zertifikat Erweiterung, die erweiterte Informationen über die beabsichtigte Verwendung des öffentlichen Schlüssels eines Zertifikats enthält.<br/>                                                                                                      | 21    |
| **Erweiterung für CAPICOM- \_ OID- \_ Zertifikat \_ Vorlagen \_**            | Bei dem Objekt handelt es sich um eine Zertifikat Erweiterung, die eine Zertifikat Vorlage enthält.<br/>                                                                                                                                                         | 22    |
| **Erweiterung "CAPICOM \_ OID \_ Application \_ CERT \_ Policies \_ "**      | Das-Objekt ist eine Zertifikat Erweiterung, die die Anwendungs Richtlinie des Zertifikats enthält.<br/>                                                                                                                                      | 23    |
| **Erweiterung der Zuordnungen von CAPICOM- \_ OID- \_ Anwendungs \_ Richtlinien \_ \_**    | Das-Objekt ist eine Zertifikat Erweiterung, die Zuordnungen zwischen verschiedenen Anwendungsrichtlinien enthält.<br/>                                                                                                                                | 24    |
| **Erweiterung für CAPICOM \_ OID- \_ Anwendungs \_ Richtlinien \_ Einschränkungen \_** | Das-Objekt ist eine Zertifikat Erweiterung, die die Anwendungsrichtlinien Einschränkungen des Zertifikats enthält.<br/>                                                                                                                          | 25    |
| **\_ \_ \_ Informations \_ Zugriffs \_ Erweiterung für CAPICOM OID Authority**          | Das-Objekt ist eine Zertifikat Erweiterung, mit der angegeben wird, wie auf Zertifizierungsstellen Informationen und-Dienste für den Aussteller des Zertifikats zugegriffen werden soll.<br/>                                                                                                   | 26    |
| **CAPICOM \_ OID \_ Server \_ auth \_ EKU**                           | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat zum Authentifizieren eines Servers verwendet werden kann.<br/>                                                                                                                | 100   |
| **CAPICOM \_ OID \_ Client \_ auth \_ EKU**                           | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat zum Authentifizieren eines Clients verwendet werden kann.<br/>                                                                                                                | 101   |
| **CAPICOM \_ OID \_ Code \_ SIGNING \_ EKU**                          | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat zum Erstellen einer digitalen Signatur verwendet werden kann.<br/>                                                                                                           | 102   |
| **CAPICOM \_ \_ -OID-e-Mail- \_ Schutz \_ EKU**                      | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für den e-Mail-Schutz verwendet werden kann.<br/>                                                                                                                    | 103   |
| **CAPICOM \_ OID- \_ IPSec- \_ \_ Endsystem- \_ EKU**                     | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für ein IPSec-Endsystem verwendet werden kann.<br/>                                                                                                                 | 104   |
| **CAPICOM \_ OID- \_ IPSec- \_ Tunnel- \_ EKU**                          | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für die IPSec-Tunnelung verwendet werden kann.<br/>                                                                                                                     | 105   |
| **CAPICOM \_ OID- \_ IPSec- \_ Benutzer- \_ EKU**                            | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für einen IPSec-Benutzer verwendet werden kann.<br/>                                                                                                                       | 106   |
| **CAPICOM \_ OID- \_ Zeit \_ Stempel \_ EKU**                         | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat zum Zeitstempel verwendet werden kann.<br/>                                                                                                                       | 107   |
| **CAPICOM \_ OID \_ CTL \_ Usage \_ SIGNING \_ EKU**                    | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat zum Signieren der Zertifikats Vertrauens Liste verwendet werden kann.<br/>                                                                                                | 108   |
| **der CAPICOM \_ OID- \_ Zeit \_ Stempel \_ Signatur- \_ EKU**                   | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat zum Signieren eines Zeitstempels verwendet werden kann.<br/>                                                                                                                    | 109   |
| **CAPICOM \_ OID \_ Server \_ Gated \_ Crypto \_ EKU**                  | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für [*Server Gated Kryptografie*](../secgloss/s-gly.md) (SGC) verwendet werden kann.<br/> | 110   |
| **CAPICOM \_ OID \_ verschlüsselndes \_ Datei \_ System \_ EKU**               | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für die [*verschlüsselndes Dateisystem*](../secgloss/e-gly.md) (EFS) verwendet werden kann.<br/>      | 111   |
| **CAPICOM \_ OID \_ EFS \_ Recovery \_ EKU**                          | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für die Wiederherstellung des EFS verwendet werden kann.<br/>                                                                                                                 | 112   |
| **CAPICOM \_ OID \_ WHQL \_ - \_ kryptografieku**                           | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für die Windows Hardware Quality Labs (WHQL)-Kryptografie verwendet werden kann.<br/>                                                                                   | 113   |
| **CAPICOM \_ OID \_ NT5 \_ \_ kryptografieku**                            | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für die Kryptografie von Windows Server 2003 und Windows XP verwendet werden kann.<br/>                                                                                     | 114   |
| **CAPICOM \_ OID \_ OEM \_ WHQL \_ Crypto \_ EKU**                      | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für die Original Gerätehersteller (OEM) WHQL Cryptography verwendet werden kann.<br/>                                                                            | 115   |
| **CAPICOM- \_ OID, \_ NT- \_ \_ \_ kryptografieku**                    | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für die Windows NT Embedded-Kryptografie verwendet werden kann.<br/>                                                                                                    | 116   |
| **CAPICOM \_ OID \_ root \_ List \_ Signatur Geber \_ EKU**                     | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat zum Signieren einer Stamm Liste verwendet werden kann.<br/>                                                                                                                     | 117   |
| **CAPICOM- \_ OID, \_ qualifizierte unter \_ Ordnung \_ EKU**               | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für die qualifizierte Unterordnung verwendet werden kann.<br/>                                                                                                             | 118   |
| **EKU für CAPICOM- \_ OID- \_ Schlüssel \_ Wiederherstellung \_**                          | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für die Schlüsselwiederherstellung verwendet werden kann.<br/>                                                                                                                        | 119   |
| **CAPICOM \_ OID \_ Digital \_ Rights \_ EKU**                        | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für digitale Rechte verwendet werden kann.<br/>                                                                                                                      | 120   |
| **CAPICOM- \_ OID- \_ Lizenzen \_ EKU**                               | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für Lizenzen verwendet werden kann.<br/>                                                                                                                            | 121   |
| **CAPICOM \_ OID \_ License \_ Server \_ EKU**                        | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für einen Lizenzserver verwendet werden kann.<br/>                                                                                                                    | 122   |
| **CAPICOM \_ OID \_ \_ Smartcard \_ Logon- \_ EKU**                     | Das-Objekt ist ein [**EKU**](eku.md) -Objekt, das angibt, dass das Zertifikat für die Smartcard-Anmeldung verwendet werden kann.<br/>                                                                                                                    | 123   |
| **CPS für den Qualifizierer der CAPICOM- \_ OID \_ PKIX \_ \_ \_**                | Bei dem Objekt handelt es sich um eine Zertifizierungs Praxis Anweisung (CPS), die für den PKIX-Richtlinien Qualifizierer der Public Key-Infrastruktur verwendet werden kann.<br/>                                                                                            | 124   |
| **CAPICOM \_ OID \_ PKIX- \_ Richtlinien \_ Qualifizierer \_ usernotice**         | Das-Objekt ist eine Benutzer Benachrichtigung, die für den PKIX-Richtlinien Qualifizierer der Public Key-Infrastruktur verwendet werden kann.<br/>                                                                                                                       | 125   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|--------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                |
| Header<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
