---
description: Stellt Dienste zur Verfügung, mit denen Anwendungsentwickler Anwendungen Sicherheit basierend auf Kryptografie hinzufügen können.
ms.assetid: 9a2add82-53f9-49ed-b20c-019f95e7d260
title: CAPICOM-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94bd7f8c2052f53b4dc1e244251ba76c1b10e349e0f43434a926db6dbeb9190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772111"
---
# <a name="capicom-reference"></a>CAPICOM-Referenz

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Der CAPICOM COM-Client stellt Dienste zur Verfügung, mit denen Anwendungsentwickler Anwendungen Sicherheit basierend auf [*Kryptografie*](../secgloss/c-gly.md) hinzufügen können. CryptoAPI umfasst Funktionen für [](../secgloss/d-gly.md)die Authentifizierung mit digitalen Signaturen, zum Umhing von Nachrichten und zum Verschlüsseln und Entschlüsseln von Daten.



| Kategorie                    | Beschreibung                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Certificate Store Objects   | Objekte, die für die Verwendung von Zertifikatspeichern und die Zertifikate in diesen Speichern verfügbar sind.                                       |
| Digitale Signaturobjekte   | Objekte, die zum digitalen Signieren von Daten und zum Überprüfen digitaler Signaturen verwendet werden.                                                      |
| Umschlagdatenobjekte      | Objekte, die verwendet werden, um umhumhierte Datennachrichten für den Datenschutz zu erstellen und Daten in umhumschlagten Nachrichten zu entschlüsseln.                      |
| Datenverschlüsselungsobjekte     | Objekte, die zum Verschlüsseln von Daten und Entschlüsseln verschlüsselter Daten verwendet werden.                                                                |
| Hilfsobjekte           | Objekte, die zum Ändern des Standardverhaltens und zum Verwalten von Zertifikaten, Zertifikatspeichern und Benutzeroberflächennachrichten verwendet werden. |
| Interoperabilitätsschnittstellen | Schnittstellen, die die Zusammenarbeit von CryptoAPI mit CAPICOM 2.0 ermöglichen.                                          |
| Enumerationstypen           | Enumerationstypen, die mit CAPICOM verwendet werden.                                                                                       |



 

## <a name="certificate-store-objects"></a>Certificate Store Objects

Die folgenden Objekte funktionieren mit [*Zertifikatspeichern*](../secgloss/c-gly.md) und den Zertifikaten in diesen Speichern. CAPICOM unterstützt die Verwendung von Zertifikatspeichern des aktuellen Benutzers, des lokalen Computers, des Arbeitsspeichers und von Active Directory.



| Object                                             | BESCHREIBUNG                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Zertifikat**](certificate.md)                 | Ein einzelnes digitales Zertifikat.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Eine Auflistung von [**PolicyInformation-Objekten.**](policyinformation.md)                                                 |
| [**Zertifikate**](certificates.md)               | Sammlung von [**Zertifikatobjekten.**](certificate.md)                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Stellt Statusinformationen zu einem Zertifikat zur Verfügung.                                                                           |
| [**Kette**](chain.md)                             | Erstellt und überprüft eine Zertifikatvalidierungskette basierend auf einem digitalen Zertifikat.                                       |
| [**Extendedproperties**](extendedproperties.md)   | Stellt eine Auflistung von [**ExtendedProperty-Objekten**](extendedproperty.md) dar.                                        |
| [**Extendedproperty**](extendedproperty.md)       | Stellt eine von Microsoft erweiterte Eigenschaft dar.                                                                               |
| [**Erweiterung**](extension.md)                     | Stellt eine einzelne Zertifikaterweiterung dar.                                                                              |
| [**Erweiterungen**](extensions.md)                   | Stellt eine Auflistung von [**Extension-Objekten**](extension.md) dar.                                                      |
| [**PrivateKey**](privatekey.md)                   | Stellt einen privaten Schlüssel dar.                                                                                               |
| [**Publickey**](publickey.md)                     | Stellt einen öffentlichen Schlüssel in einem [**Certificate-Objekt**](certificate.md) dar.                                                 |
| [**Speicher**](store.md)                             | Stellt die Eigenschaften und Methoden zum Auswählen, Verwalten und Verwenden von Zertifikatspeichern und Zertifikaten in diesen Speichern zur Auswahl, Verwaltung und Verwendung zur Auswahl. |
| [**Vorlage**](template.md)                       | Stellt die Zertifikaterweiterungsvorlage des Zertifikats dar.                                                       |



 

## <a name="digital-signature-objects"></a>Digitale Signaturobjekte

Die folgenden Objekte werden exportiert, um Daten digital zu signieren und digitale Signaturen zu überprüfen.



| Object                           | BESCHREIBUNG                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Stellt Funktionen zum Signieren von Inhalten mit einer digitalen Authenticode-Signatur zur Verfügung. |
| [**SignedData**](signeddata.md) | Objekt, das zum Signieren von Daten und zum Überprüfen der Signatur signierter Daten verwendet wird.               |
| [**Signer**](signer.md)         | Informationen zu einem einzelnen Daten signieren, einschließlich des Zertifikats des Signers.           |
| [**Unterzeichner**](signers.md)       | Sammlung von [**Signer-Objekten.**](signer.md)                                    |



 

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
| [**Oid**](oid.md)                             | Stellt einen Objektbezeichner dar, der von mehreren CAPICOM-Eigenschaften verwendet wird.                                                                     |
| [**OIDs**](oids.md)                           | Stellt eine Auflistung von [**OID-Objekten**](oid.md) dar.                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Ermöglicht den Zugriff auf die Richtlinien-OIDs einer Erweiterung.                                                                                             |
| [**Qualifizierer**](qualifier.md)                 | Stellt einen CPS-Zeiger (Certification Practice Statement) oder einen Benutzerhinweisqualifizierer dar.                                                           |
| [**Qualifikation**](qualifiers.md)               | Stellt eine Auflistung von Qualifizierern dar.                                                                                                          |
| [**Einstellungen**](settings.md)                   | Aktiviert oder deaktiviert Dialogfelder, um zur Eingabe der Signator- oder Absenderidentität aufzugeben, wenn diese Identität nicht angegeben ist.                                     |
| [**Hilfsprogramme**](utilities.md)                 | Stellt Funktionen für allgemeine Aufgaben zur Verfügung.                                                                                                        |



 

## <a name="interoperability-interfaces"></a>Interoperabilitätsschnittstellen

Die folgenden Schnittstellen ermöglichen die Zusammenarbeit von CryptoAPI mit CAPICOM 2.0.



| Schnittstelle                              | BESCHREIBUNG                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Ermöglicht den Zugriff auf den Kontext eines CAPICOM [](certificate.md) X.509v3-Zertifikatobjekts. Dieser Kontext ermöglicht die Verwendung des CAPICOM-Zertifikats in anderen Ableitungen von CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Ermöglicht den Zugriff auf den [](store.md) Kontext eines CAPICOM-Store Objekts. Dieser Kontext ermöglicht die Verwendung des CAPICOM-Zertifikatspeichers in anderen Ableitungen von CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Ermöglicht den Zugriff auf den Kontext eines CAPICOM [**Chain-Objekts.**](chain.md) Dieser Kontext ermöglicht die Verwendung der CAPICOM-Zertifikatvertrauenskette in anderen Ableitungen von CryptoAPI.         |



 

## <a name="enumeration-types"></a>Enumerationstypen

CAPICOM definiert die folgenden Enumerationstypen:

-   [**CAPICOM \_ ACTIVE \_ DIRECTORY \_ SEARCH \_ LOCATION**](capicom-active-directory-search-location.md)
-   [**CAPICOM-ATTRIBUT \_**](capicom-attribute.md)
-   [**\_ \_ CAPICOM-ZERTIFIKATINFORMATIONSTYP \_**](capicom-cert-info-type.md)
-   [**CAPICOM \_ CERTIFICATE \_ FIND \_ TYPE**](capicom-certificate-find-type.md)
-   [**CAPICOM \_ CERTIFICATE \_ \_ INCLUDE-OPTION**](capicom-certificate-include-option.md)
-   [**CAPICOM \_ CERTIFICATE \_ SAVE \_ AS \_ TYPE**](capicom-certificate-save-as-type.md)
-   [**\_CAPICOM-ZERTIFIKATE \_ SPEICHERN ALS \_ \_ TYP**](capicom-certificates-save-as-type.md)
-   [**\_CAPICOM-HÄKCHEN \_**](capicom-check-flag.md)
-   [**\_CAPICOM-EKU**](capicom-eku.md)
-   [**\_CAPICOM-CODIERUNGSTYP \_**](capicom-encoding-type.md)
-   [**\_CAPICOM-VERSCHLÜSSELUNGSALGORITHMUS \_**](capicom-encryption-algorithm.md)
-   [**\_CAPICOM-VERSCHLÜSSELUNGSSCHLÜSSELLÄNGE \_ \_**](capicom-encryption-key-length.md)
-   [**\_CAPICOM-FEHLERCODE \_**](capicom-error-code.md)
-   [**\_CAPICOM-EXPORTFLAG \_**](capicom-export-flag.md)
-   [**\_CAPICOM-HASHALGORITHMUS \_**](capicom-hash-algorithm.md)
-   [**CAPICOM \_ KEY \_ LOCATION**](capicom-key-location.md)
-   [**\_CAPICOM-SCHLÜSSELSPEZIFIKATION \_**](capicom-key-spec.md)
-   [**\_ \_ CAPICOM-SCHLÜSSELSPEICHERFLAG \_**](capicom-key-storage-flag.md)
-   [**\_CAPICOM-OID**](capicom-oid.md)
-   [**CAPICOM \_ PROPID**](capicom-propid.md)
-   [**CAPICOM \_ \_ PROV-TYP**](capicom-prov-type.md)
-   [**\_CAPICOM-GEHEIMNISTYP \_**](capicom-secret-type.md)
-   [**CAPICOM \_ SIGNED \_ DATA \_ VERIFY \_ FLAG**](capicom-signed-data-verify-flag.md)
-   [**CAPICOM \_ STORE \_ LOCATION**](capicom-store-location.md)
-   [**CAPICOM \_ STORE \_ OPEN \_ MODE**](capicom-store-open-mode.md)
-   [**CAPICOM \_ STORE \_ SAVE \_ AS \_ TYPE**](capicom-store-save-as-type.md)

 

 
