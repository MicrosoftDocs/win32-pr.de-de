---
description: Listet die von CryptoAPI bereitgestellten Objekte auf.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Kryptografieobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea3476e7edad1d32fe1e11635bd65622d2a8375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393505"
---
# <a name="cryptography-objects"></a>Kryptografieobjekte

Kryptografieobjekte werden gemäß der Verwendung wie folgt kategorisiert:

-   [Zertifikat Speicher Objekte](#certificate-store-objects)
-   [Digitale Signatur Objekte](#digital-signature-objects)
-   [Eingeschlossene Datenobjekte](#enveloped-data-objects)
-   [Daten Verschlüsselungs Objekte](#data-encryption-objects)
-   [Hilfsobjekte](#auxiliary-objects)
-   [Zertifikat Registrierungs Objekte](#certificate-enrollment-objects)

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
| [**ExtendedProperty**](extendedproperties.md)     | Stellt eine von Microsoft erweiterte Eigenschaft dar.                                                                               |
| [**Erweiterung**](extension.md)                     | Stellt eine einzelne Zertifikat Erweiterung dar.                                                                              |
| [**Erweiterungen**](extensions.md)                   | Stellt eine Auflistung von [**Erweiterungs**](extension.md) Objekten dar.                                                      |
| [**PrivateKey**](privatekey.md)                   | Stellt einen privaten Schlüssel dar.                                                                                               |
| [**PublicKey**](publickey.md)                     | Stellt einen öffentlichen Schlüssel in einem [**Zertifikat**](certificate.md) Objekt dar.                                                 |
| [**Speicher**](store.md)                             | Stellt die Eigenschaften und Methoden bereit, mit denen Sie Zertifikat Speicher und die Zertifikate in diesen speichern auswählen, verwalten und verwenden können. |
| [**Vorlage**](template.md)                       | Stellt die Zertifikat Erweiterungs Vorlage des Zertifikats dar.                                                       |



 

## <a name="digital-signature-objects"></a>Digitale Signatur Objekte

Die folgenden Objekte werden exportiert, um Daten digital zu signieren und digitale Signaturen zu überprüfen.



| Object                           | BESCHREIBUNG                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**Signedcode**](signedcode.md) | Objekt, das zum Signieren von Code mit einer digitalen Authenticode-Signatur und zum Überprüfen der Signatur für signierten Code verwendet wird. |
| [**SignedData**](signeddata.md) | Zum Signieren von Daten und zum Überprüfen der Signatur von signierten Daten verwendetes Objekt.                                        |
| [**Signatur Geber**](signer.md)         | Informationen zu einem einzelnen Daten Signatur Geber, einschließlich des Zertifikats des Signatur Gebers.                                    |
| [**Signatur Geber**](signers.md)       | Sammlung von [**Signatur**](signer.md) Geber Objekten.                                                             |



 

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
| [**Benachrichtifür Notierungen**](noticenumbers.md)         | Stellt eine Auflistung von [**Erweiterungs**](extension.md) Objekten dar.                                                                              |
| [**OID**](oid.md)                             | Stellt einen Objekt Bezeichner dar, der von mehreren CAPICOM-Eigenschaften verwendet wird.                                                                     |
| [**OIDs**](oids.md)                           | Stellt eine Auflistung von [**OID**](oid.md) -Objekten dar.                                                                                          |
| [**Policyinformation**](policyinformation.md) | Bietet Zugriff auf die OIDs der Richtlinie einer Erweiterung.                                                                                             |
| [**Qualifizierer**](qualifier.md)                 | Stellt einen CPS-Zeiger (Certification Practice Statement) oder einen Benutzer Hinweis Qualifizierer dar.                                                           |
| [**Qualifikation**](qualifiers.md)               | Stellt eine Auflistung von Qualifizierern dar.                                                                                                          |
| [**Einstellungen**](settings.md)                   | Aktiviert oder deaktiviert Dialogfelder, um zur Eingabe des Signatur Gebers oder der Absender Identität aufzufordern, wenn diese Identität nicht angegeben ist.                                     |
| [**Versorgungsunternehmen**](utilities.md)                 | Stellt Funktionen für häufige Aufgaben bereit.                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a>Zertifikat Registrierungs Objekte

Das folgende Objekt wird für die Zertifikat Registrierung verwendet.



| Object                     | BESCHREIBUNG                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) | Objekt, das das Zertifikat Registrierungs Steuerelement darstellt. Sie wird in erster Linie verwendet, wenn Sie in Visual Basic oder einer anderen Automatisierungs Sprache programmieren. |



 

 

 
