---
description: Bietet Dienste, die Anwendungsentwicklern das Hinzufügen von Sicherheit auf der Grundlage der Kryptografie für Anwendungen ermöglichen.
ms.assetid: 9a2add82-53f9-49ed-b20c-019f95e7d260
title: CAPICOM-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b828f3b5b35e3e0ef799529f866c23416c8df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366297"
---
# <a name="capicom-reference"></a>CAPICOM-Referenz

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Der CAPICOM-com-Client stellt Dienste bereit, die es Anwendungsentwicklern ermöglichen, Sicherheit basierend auf der [*Kryptografie*](../secgloss/c-gly.md) für Anwendungen hinzuzufügen. CryptoAPI umfasst Funktionen für die Authentifizierung mithilfe [*digitaler Signaturen*](../secgloss/d-gly.md), für das umschließen von Nachrichten und zum Verschlüsseln und Entschlüsseln von Daten.



| Category                    | BESCHREIBUNG                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Zertifikat Speicher Objekte   | Objekte, die für die Verwendung von Zertifikat speichern und Zertifikaten in diesen speichern verfügbar sind.                                       |
| Digitale Signatur Objekte   | Objekte, mit denen Daten digital signiert und digitale Signaturen überprüft werden.                                                      |
| Eingeschlossene Datenobjekte      | Objekte, die verwendet werden, um eingeschlossene Daten Nachrichten für den Datenschutz zu erstellen und um Daten in eingeschlossenen Nachrichten zu entschlüsseln.                      |
| Daten Verschlüsselungs Objekte     | -Objekte, die zum Verschlüsseln von Daten und zum Entschlüsseln verschlüsselter Daten verwendet werden.                                                                |
| Hilfsobjekte           | Objekte, mit denen Standardverhalten geändert und Zertifikate, Zertifikat Speicher und Benutzeroberflächen Meldungen verwaltet werden. |
| Interoperabilitäts Schnittstellen | Schnittstellen, die die Ableitung von CryptoAPI für die Zusammenarbeit mit CAPICOM 2,0 ermöglichen.                                          |
| Enumerationstypen           | Mit CAPICOM verwendete Enumerationstypen.                                                                                       |



 

## <a name="certificate-store-objects"></a>Zertifikat Speicher Objekte

Die folgenden Objekte funktionieren mit [*Zertifikat speichern*](../secgloss/c-gly.md) und den Zertifikaten in diesen speichern. CAPICOM unterstützt die Verwendung aktueller Benutzer, lokaler Computer, Arbeitsspeicher und Active Directory Zertifikat Speicher.



| Object                                             | BESCHREIBUNG                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Stellt**](certificate.md)                 | Ein einzelnes digitales Zertifikat.                                                                                           |
| [**Certificatepolicies**](certificatepolicies.md) | Eine Auflistung von [**policyinformation**](policyinformation.md) -Objekten.                                                 |
| [**Zertifikate**](certificates.md)               | Sammlung von [**Zertifikat**](certificate.md) Objekten.                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Stellt Statusinformationen zu einem Zertifikat bereit.                                                                           |
| [**Ketten**](chain.md)                             | Erstellt und überprüft eine Zertifikat Validierungs Kette auf der Grundlage eines digitalen Zertifikats.                                       |
| [**ExtendedProperties**](extendedproperties.md)   | Stellt eine Auflistung von [**ExtendedProperty**](extendedproperty.md) -Objekten dar.                                        |
| [**ExtendedProperty**](extendedproperty.md)       | Stellt eine von Microsoft erweiterte Eigenschaft dar.                                                                               |
| [**Erweiterung**](extension.md)                     | Stellt eine einzelne Zertifikat Erweiterung dar.                                                                              |
| [**Erweiterungen**](extensions.md)                   | Stellt eine Auflistung von [**Erweiterungs**](extension.md) Objekten dar.                                                      |
| [**PrivateKey**](privatekey.md)                   | Stellt einen privaten Schlüssel dar.                                                                                               |
| [**PublicKey**](publickey.md)                     | Stellt einen öffentlichen Schlüssel in einem [**Zertifikat**](certificate.md) Objekt dar.                                                 |
| [**Speicher**](store.md)                             | Stellt die Eigenschaften und Methoden bereit, mit denen Sie Zertifikat Speicher und die Zertifikate in diesen speichern auswählen, verwalten und verwenden können. |
| [**Vorlage**](template.md)                       | Stellt die Zertifikat Erweiterungs Vorlage des Zertifikats dar.                                                       |



 

## <a name="digital-signature-objects"></a>Digitale Signatur Objekte

Die folgenden Objekte werden exportiert, um Daten digital zu signieren und digitale Signaturen zu überprüfen.



| Object                           | BESCHREIBUNG                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| [**Signedcode**](signedcode.md) | Stellt Funktionen zum Signieren von Inhalt mit einer digitalen Authenticode-Signatur bereit. |
| [**SignedData**](signeddata.md) | Zum Signieren von Daten und zum Überprüfen der Signatur von signierten Daten verwendetes Objekt.               |
| [**Signatur Geber**](signer.md)         | Informationen zu einem einzelnen Daten Signatur Geber, einschließlich des Zertifikats des Signatur Gebers.           |
| [**Signatur Geber**](signers.md)       | Sammlung von [**Signatur**](signer.md) Geber Objekten.                                    |



 

## <a name="enveloped-data-objects"></a>Eingeschlossene Datenobjekte

Die folgenden Objekte werden exportiert, um eingehüllte Daten Nachrichten für den Datenschutz zu erstellen und um Daten in eingeschlossenen Nachrichten zu entschlüsseln.



| Object                                 | BESCHREIBUNG                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnvelopedData**](envelopeddata.md) | -Objekte, die zum Erstellen, senden und empfangen von Daten verwendet werden. Eingeschlossene Daten werden so verschlüsselt, dass Sie nur von den vorgesehenen Empfängern entschlüsselt werden können. |
| [**Empfänger**](recipients.md)       | Sammlung der [**Zertifikat**](certificate.md) Objekte der vorgesehenen Empfänger einer eingeschlossenen Nachricht.                           |



 

## <a name="data-encryption-objects"></a>Daten Verschlüsselungs Objekte

Das folgende Objekt wird exportiert, um beliebige Daten für den Datenschutz zu verschlüsseln und verschlüsselte Daten zu entschlüsseln.



| Object                                 | BESCHREIBUNG                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**EncryptedData**](encrypteddata.md) | Objekte, die zum Verschlüsseln von Daten verwendet werden. Verschlüsselte Daten in einem [**verschlüsselteddata**](encrypteddata.md) -Objekt können entschlüsselt werden. |



 

## <a name="auxiliary-objects"></a>Hilfsobjekte

Die folgenden Objekte werden exportiert, um das Standardverhalten anderer Objekte zu ändern und um Zertifikate, Zertifikat Speicher und Nachrichten zu verwalten.



| Object                                         | BESCHREIBUNG                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithmus**](algorithm.md)                 | Legt den Algorithmus und die [*Schlüssellänge*](../secgloss/k-gly.md) fest, die bei kryptografischen Vorgängen verwendet werden sollen. |
| [**Versehen**](attribute.md)                 | Bietet ein einzelnes Element mit zusätzlichen Informationen über eine Signatur, z. b. den Zeitpunkt der Signierung.                                                    |
| [**Attribute**](attributes.md)               | Sammlung von [**Attribut**](attribute.md) Objekten.                                                                                           |
| [**Basiceinschränkungen**](basicconstraints.md)   | Bietet schreibgeschützten Zugriff auf grundlegende Einschränkungen der Verwendung eines Zertifikats.                                                                    |
| [**EKU**](eku.md)                             | Bietet Zugriff auf EKU-Eigenschaften von Zertifikaten.                                                                                              |
| [**EKUs**](ekus.md)                           | Sammlung von [**EKU**](eku.md) -Objekten.                                                                                                       |
| [**Encoddata**](encodeddata.md)             | Stellt einen Block codierter Daten dar.                                                                                                             |
| [**Extendedkeyusage**](extendedkeyusage.md)   | Bietet schreibgeschützten Zugriff auf die Eigenschaften der erweiterten Schlüssel Verwendung von Zertifikaten.                                                                 |
| [**HashedData**](hasheddata.md)               | Bietet Funktionen zum Anwenden eines Hash Algorithmus auf eine Zeichenfolge.                                                                               |
| [**Endeinheits Zertifikaten der**](keyusage.md)                   | Bietet schreibgeschützten Zugriff auf Schlüssel Verwendungs Eigenschaften von Zertifikaten.                                                                              |
| [**OID**](oid.md)                             | Stellt einen Objekt Bezeichner dar, der von mehreren CAPICOM-Eigenschaften verwendet wird.                                                                     |
| [**OIDs**](oids.md)                           | Stellt eine Auflistung von [**OID**](oid.md) -Objekten dar.                                                                                          |
| [**Policyinformation**](policyinformation.md) | Bietet Zugriff auf die OIDs der Richtlinie einer Erweiterung.                                                                                             |
| [**Qualifizierer**](qualifier.md)                 | Stellt einen CPS-Zeiger (Certification Practice Statement) oder einen Benutzer Hinweis Qualifizierer dar.                                                           |
| [**Qualifikation**](qualifiers.md)               | Stellt eine Auflistung von Qualifizierern dar.                                                                                                          |
| [**Einstellungen**](settings.md)                   | Aktiviert oder deaktiviert Dialogfelder, um zur Eingabe des Signatur Gebers oder der Absender Identität aufzufordern, wenn diese Identität nicht angegeben ist.                                     |
| [**Versorgungsunternehmen**](utilities.md)                 | Stellt Funktionen für häufige Aufgaben bereit.                                                                                                        |



 

## <a name="interoperability-interfaces"></a>Interoperabilitäts Schnittstellen

Die folgenden Schnittstellen ermöglichen die Ableitung von CryptoAPI für die Zusammenarbeit mit CAPICOM 2,0.



| Schnittstelle                              | BESCHREIBUNG                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Icertcontext**](icertcontext.md)   | Bietet Zugriff auf den Kontext eines CAPICOM X. 509v3- [**Zertifikat**](certificate.md) Objekts. In diesem Kontext kann das CAPICOM-Zertifikat in anderen Ableitungen von CryptoAPI verwendet werden. |
| [**Icertstore**](icertstore.md)       | Bietet Zugriff auf den Kontext eines CAPICOM- [**Speicher**](store.md) Objekts. In diesem Kontext kann der CAPICOM-Zertifikat Speicher in anderen Ableitungen von CryptoAPI verwendet werden.               |
| [**Ichaincontext**](ichaincontext.md) | Bietet Zugriff auf den Kontext eines CAPICOM- [**Ketten**](chain.md) Objekts. In diesem Kontext kann die CAPICOM-Zertifikats Vertrauenskette in anderen Ableitungen von CryptoAPI verwendet werden.         |



 

## <a name="enumeration-types"></a>Enumerationstypen

CAPICOM definiert die folgenden Enumerationstypen:

-   [**CAPICOM- \_ Active \_ Directory- \_ Such \_ Speicherort**](capicom-active-directory-search-location.md)
-   [**CAPICOM- \_ Attribut**](capicom-attribute.md)
-   [**CAPICOM- \_ CERT- \_ \_ Informationstyp**](capicom-cert-info-type.md)
-   [**CAPICOM \_ - \_ zertifikatsuchtyp \_**](capicom-certificate-find-type.md)
-   [**CAPICOM \_ Certificate \_ include- \_ Option**](capicom-certificate-include-option.md)
-   [**\_ \_ \_ Dateityp des CAPICOM-Zertifikats \_**](capicom-certificate-save-as-type.md)
-   [**CAPICOM- \_ Zertifikate \_ Speichern als- \_ \_ Typ**](capicom-certificates-save-as-type.md)
-   [**CAPICOM- \_ Häkchen \_**](capicom-check-flag.md)
-   [**CAPICOM- \_ EKU**](capicom-eku.md)
-   [**CAPICOM \_ - \_ Codierungstyp**](capicom-encoding-type.md)
-   [**CAPICOM- \_ Verschlüsselungs \_ Algorithmus**](capicom-encryption-algorithm.md)
-   [**Länge des CAPICOM- \_ Verschlüsselungs \_ Schlüssels \_**](capicom-encryption-key-length.md)
-   [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md)
-   [**CAPICOM \_ - \_ exportflag**](capicom-export-flag.md)
-   [**CAPICOM- \_ Hash \_ Algorithmus**](capicom-hash-algorithm.md)
-   [**CAPICOM- \_ Schlüssel \_ Speicherort**](capicom-key-location.md)
-   [**CAPICOM- \_ Schlüssel \_ Spezifikation**](capicom-key-spec.md)
-   [**CAPICOM \_ Key \_ Storage- \_ Flag**](capicom-key-storage-flag.md)
-   [**CAPICOM- \_ OID**](capicom-oid.md)
-   [**CAPICOM- \_ PROPID**](capicom-propid.md)
-   [**CAPICOM \_ Prov- \_ Typ**](capicom-prov-type.md)
-   [**CAPICOM- \_ geheimer \_ Typ**](capicom-secret-type.md)
-   [**CAPICOM \_ - \_ \_ Flag zur Überprüfung signierter Daten \_**](capicom-signed-data-verify-flag.md)
-   [**CAPICOM \_ - \_ Speicherort**](capicom-store-location.md)
-   [**CAPICOM \_ Store- \_ Öffnungs \_ Modus**](capicom-store-open-mode.md)
-   [**\_ \_ \_ Dateityp für CAPICOM-Speicher \_**](capicom-store-save-as-type.md)

 

 
