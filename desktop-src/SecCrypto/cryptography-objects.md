---
description: Listet die von CryptoAPI bereitgestellten Objekte auf.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Kryptografieobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff5e9495d64c38272bac54ffac03d1d087b9286887b4e4e520c6a447765efac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768372"
---
# <a name="cryptography-objects"></a>Kryptografieobjekte

Kryptografieobjekte werden nach Verwendung wie folgt kategorisiert:

-   [Certificate Store Objects](#certificate-store-objects)
-   [Digitale Signaturobjekte](#digital-signature-objects)
-   [Umschlagdatenobjekte](#enveloped-data-objects)
-   [Datenverschlüsselungsobjekte](#data-encryption-objects)
-   [Hilfsobjekte](#auxiliary-objects)
-   [Zertifikatregistrierungsobjekte](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a>Certificate Store Objects

Die folgenden Objekte funktionieren mit [*Zertifikatspeichern*](../secgloss/c-gly.md) und den Zertifikaten in diesen Speichern. CAPICOM unterstützt die Verwendung von Aktuellen Benutzer-, lokalen Computer-, Arbeitsspeicher- und Active Directory-Zertifikatspeichern.



| Object                                             | BESCHREIBUNG                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Zertifikat**](certificate.md)                 | Ein einzelnes digitales Zertifikat.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Eine Auflistung von [**PolicyInformation-Objekten.**](policyinformation.md)                                                 |
| [**Zertifikate**](certificates.md)               | Sammlung von [**Zertifikatobjekten.**](certificate.md)                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Stellt Statusinformationen zu einem Zertifikat zur Verfügung.                                                                           |
| [**Kette**](chain.md)                             | Erstellt und überprüft eine Zertifikatvalidierungskette basierend auf einem digitalen Zertifikat.                                       |
| [**Extendedproperties**](extendedproperties.md)   | Stellt eine Auflistung von [**ExtendedProperty-Objekten**](extendedproperty.md) dar.                                        |
| [**Extendedproperty**](extendedproperties.md)     | Stellt eine von Microsoft erweiterte Eigenschaft dar.                                                                               |
| [**Erweiterung**](extension.md)                     | Stellt eine einzelne Zertifikaterweiterung dar.                                                                              |
| [**Erweiterungen**](extensions.md)                   | Stellt eine Auflistung von [**Extension-Objekten**](extension.md) dar.                                                      |
| [**PrivateKey**](privatekey.md)                   | Stellt einen privaten Schlüssel dar.                                                                                               |
| [**Publickey**](publickey.md)                     | Stellt einen öffentlichen Schlüssel in einem [**Certificate-Objekt**](certificate.md) dar.                                                 |
| [**Speicher**](store.md)                             | Stellt die Eigenschaften und Methoden zum Auswählen, Verwalten und Verwenden von Zertifikatspeichern und Zertifikaten in diesen Speichern zur Auswahl, Verwaltung und Verwendung zur Auswahl. |
| [**Vorlage**](template.md)                       | Stellt die Zertifikaterweiterungsvorlage des Zertifikats dar.                                                       |



 

## <a name="digital-signature-objects"></a>Digitale Signaturobjekte

Die folgenden Objekte werden exportiert, um Daten digital zu signieren und digitale Signaturen zu überprüfen.



| Object                           | BESCHREIBUNG                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Objekt, das verwendet wird, um Code mit einer digitalen Authenticode-Signatur zu signieren und die Signatur für signierten Code zu überprüfen. |
| [**SignedData**](signeddata.md) | Objekt, das zum Signieren von Daten und zum Überprüfen der Signatur signierter Daten verwendet wird.                                        |
| [**Signer**](signer.md)         | Informationen zu einem einzelnen Daten signieren, einschließlich des Zertifikats des Signers.                                    |
| [**Unterzeichner**](signers.md)       | Sammlung von [**Signer-Objekten.**](signer.md)                                                             |



 

## <a name="enveloped-data-objects"></a>Umschlagdatenobjekte

Die folgenden Objekte werden exportiert, um umhumhierte Datennachrichten für den Datenschutz zu erstellen und Daten in umumschlagten Nachrichten zu entschlüsseln.



| Object                                 | BESCHREIBUNG                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnvelopedData**](envelopeddata.md) | Objekte, die zum Erstellen, Senden und Empfangen von umhumhierten Daten verwendet werden. Umhumschlagte Daten werden verschlüsselt, sodass sie nur von den vorgesehenen Empfängern entschlüsselt werden können. |
| [**Empfänger**](recipients.md)       | Auflistung der [**Certificate-Objekte**](certificate.md) der vorgesehenen Empfänger einer umschlagenen Nachricht.                           |



 

## <a name="data-encryption-objects"></a>Datenverschlüsselungsobjekte

Das folgende Objekt wird exportiert, um beliebige Daten zum Schutz des Datenschutzes zu verschlüsseln und verschlüsselte Daten zu entschlüsseln.



| Object                                 | BESCHREIBUNG                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Encrypteddata**](encrypteddata.md) | Objekte, die zum Verschlüsseln von Daten verwendet werden. Verschlüsselte Daten in einem [**EncryptedData-Objekt**](encrypteddata.md) können entschlüsselt werden. |



 

## <a name="auxiliary-objects"></a>Hilfsobjekte

Die folgenden Objekte werden exportiert, um das Standardverhalten anderer Objekte zu ändern und Zertifikate, Zertifikatspeicher und Nachrichten zu verwalten.



| Object                                         | BESCHREIBUNG                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithmus**](algorithm.md)                 | Legt den Algorithmus und die [*Schlüssellänge fest,*](../secgloss/k-gly.md) die in kryptografischen Vorgängen verwendet werden sollen. |
| [**attribute**](attribute.md)                 | Stellt eine einzelne hinzugefügte Information über eine Signatur zur Verfügung, z. B. den Zeitpunkt der Signatur.                                                    |
| [**Attribute**](attributes.md)               | Auflistung von [**Attributobjekten.**](attribute.md)                                                                                           |
| [**BasicConstraints**](basicconstraints.md)   | Bietet schreibgeschützten Zugriff auf grundlegende Einschränkungen für die Verwendung eines Zertifikats.                                                                    |
| [**EKU**](eku.md)                             | Ermöglicht den Zugriff auf EKU-Eigenschaften von Zertifikaten.                                                                                              |
| [**EKUs**](ekus.md)                           | Auflistung von [**EKU-Objekten.**](eku.md)                                                                                                       |
| [**Codierte Daten**](encodeddata.md)             | Stellt einen Block codierter Daten dar.                                                                                                             |
| [**ExtendedKeyUsage**](extendedkeyusage.md)   | Bietet schreibgeschützten Zugriff auf die erweiterten Schlüsselverwendungseigenschaften von Zertifikaten.                                                                 |
| [**HashedData**](hasheddata.md)               | Stellt Funktionen zum Anwenden eines Hashalgorithmus auf eine Zeichenfolge zur Verfügung.                                                                               |
| [**KeyUsage**](keyusage.md)                   | Bietet schreibgeschützten Zugriff auf Schlüsselverwendungseigenschaften von Zertifikaten.                                                                              |
| [**NoticeNumbers**](noticenumbers.md)         | Stellt eine Auflistung von [**Extension-Objekten**](extension.md) dar.                                                                              |
| [**Oid**](oid.md)                             | Stellt einen Objektbezeichner dar, der von mehreren CAPICOM-Eigenschaften verwendet wird.                                                                     |
| [**OIDs**](oids.md)                           | Stellt eine Auflistung von [**OID-Objekten**](oid.md) dar.                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Ermöglicht den Zugriff auf die Richtlinien-OIDs einer Erweiterung.                                                                                             |
| [**Qualifizierer**](qualifier.md)                 | Stellt einen CPS-Zeiger (Certification Practice Statement) oder einen Qualifizierer für Benutzerhinweise dar.                                                           |
| [**Qualifikation**](qualifiers.md)               | Stellt eine Auflistung von Qualifizierern dar.                                                                                                          |
| [**Einstellungen**](settings.md)                   | Aktiviert oder deaktiviert Dialogfelder, um zur Eingabe der Signierer- oder Absenderidentität aufzufordern, wenn diese Identität nicht angegeben ist.                                     |
| [**Hilfsprogramme**](utilities.md)                 | Stellt Funktionen für allgemeine Aufgaben bereit.                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a>Zertifikatregistrierungsobjekte

Das folgende Objekt wird für die Zertifikatregistrierung verwendet.



| Object                     | BESCHREIBUNG                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) | Objekt, das das Zertifikatregistrierungssteuerelement darstellt. Sie wird hauptsächlich bei der Programmierung in Visual Basic oder einer anderen Automation-Sprache verwendet. |



 

 

 
