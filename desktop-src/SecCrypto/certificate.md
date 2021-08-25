---
description: Stellt ein einzelnes digitales Zertifikat dar.
ms.assetid: da95312b-cc9f-44f0-9517-0b28c5fcfb61
title: Zertifikatobjekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6c19acc094426f99599b9e4aa9ea3968414c7de1d99377b2ce0bd2e8e3fde05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877990"
---
# <a name="certificate-object"></a>Zertifikatobjekt

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**Namespace System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Das **Certificate-Objekt** stellt ein einzelnes [*digitales Zertifikat dar.*](../secgloss/d-gly.md)

Das **Zertifikatobjekt** macht die folgenden Schnittstellen verfügbar:

-   **ICertificate:** Eingeführt in CAPICOM 1.0.
-   **ICertificate2 :** Eingeführt in CAPICOM 2.0.

## <a name="when-to-use"></a>Verwendung

Das **Zertifikatobjekt** wird verwendet, um die folgenden Aufgaben auszuführen:

-   Laden Sie Zertifikatdaten, einschließlich des privaten Schlüssels, aus einer Datei.
-   Informationen aus dem Zertifikat.
-   Gibt grundlegende Einschränkungen, EKU, erweiterte Eigenschaften, Erweiterungen, Schlüsselverwendung, öffentlicher Schlüssel und Vorlagenobjekte zurück, die dem Zertifikat zugeordnet sind.
-   Ermitteln Sie, ob das Zertifikat gültig ist, und überprüfen Sie die Zugriffsverfügbarkeit des privaten Schlüssels des Zertifikatsubjekts.
-   Zeigt das Zertifikat an.
-   Importieren und exportieren Sie das Zertifikat.
-   Speichern Sie das Zertifikat in einer Datei.
-   Rufen Sie Eigenschaften ab, die das Zertifikat beschreiben, oder legen Sie sie fest.

## <a name="members"></a>Member

Das **Zertifikatobjekt** verfügt über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Certificate-Objekt** verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BasicConstraints**](certificate-basicconstraints.md)     | Gibt ein [**BasicConstraints-Objekt**](basicconstraints.md) zurück, das die grundlegende Einschränkungserweiterung des Zertifikats darstellt.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                   |
| [**Anzeige**](certificate-display.md)                       | Zeigt ein Zertifikat an.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                                                                                                                             |
| [**Exportieren**](certificate-export.md)                         | Kopiert ein Zertifikat in eine codierte Zeichenfolge. Die codierte Zeichenfolge kann in eine Datei geschrieben oder in ein neues **Zertifikatobjekt importiert** werden.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                               |
| [**ExtendedKeyUsage**](certificate-extendedkeyusage.md)     | Gibt ein [**ExtendedKeyUsage-Objekt**](extendedkeyusage.md) zurück, das die gültigen erweiterten Schlüssel verwendet, die das Zertifikat verwenden.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                       |
| [**Extendedproperties**](certificate-extendedproperties.md) | Gibt eine Auflistung der erweiterten Eigenschaften des Zertifikats zurück.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                             |
| [**Erweiterungen**](certificate-extensions.md)                 | Gibt eine Auflistung der Erweiterungen zurück, die dem Zertifikat zugeordnet sind.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                         |
| [**GetInfo**](certificate-getinfo.md)                       | Ruft Informationen aus dem Zertifikat ab.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                                                                                                         |
| [**HasPrivateKey**](certificate-hasprivatekey.md)           | Bestimmt, ob dem Zertifikat ein [*privater Schlüssel*](../secgloss/p-gly.md) zugeordnet ist.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                    |
| [**Importieren**](certificate-import.md)                         | Importiert ein zuvor codiertes Zertifikat aus einer Zeichenfolge in das **Zertifikatobjekt.**<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                                                             |
| [**IsValid**](certificate-isvalid.md)                       | Erstellt eine Zertifikatüberprüfungskette für ein Zertifikat und gibt ein [**CertificateStatus-Objekt**](certificatestatus.md) zurück, das den Gültigkeitsstatus des Zertifikats enthält.<br/> (Geerbt von **CertificateICertificate2ICertificate**) |
| [**KeyUsage**](certificate-keyusage.md)                     | Gibt ein [**KeyUsage-Objekt**](keyusage.md) zurück, das die gültige Schlüsselverwendung des Zertifikats angibt.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                                                |
| [**Laden**](certificate-load.md)                             | Importiert ein Zertifikat aus einer Datei.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                                                              |
| [**Publickey**](certificate-publickey.md)                   | Gibt ein [**PublicKey-Objekt**](publickey.md) zurück.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                                                |
| [**Speichern**](certificate-save.md)                             | Speichert das Zertifikat in einer Datei.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                                                                |
| [**Vorlage**](certificate-template.md)                     | Gibt die dem Zertifikat zugeordnete Vorlage zurück.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                                           |



 

### <a name="properties"></a>Eigenschaften

Das **Certificate-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp           | BESCHREIBUNG                                                                                                                                          |
|:--------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Archiviert**](certificate-archived.md)<br/>           | Lesen/Schreiben<br/> | Legt einen booleschen Wert fest, der angibt, ob das Zertifikat archiviert wird, oder ruft diesen ab.<br/> (Geerbt von **CertificateICertificate2**)       |
| [**IssuerName**](certificate-issuername.md)<br/>       | Schreibgeschützt<br/>  | Ruft eine Zeichenfolge ab, die den Namen des Zertifikatausstellers enthält.<br/> (Geerbt von **CertificateICertificate2ICertificate**)            |
| [**PrivateKey**](certificate-privatekey.md)<br/>       | Lesen/Schreiben<br/> | Legt den privaten Schlüssel fest, der dem Zertifikat zugeordnet ist, oder ruft diesen ab.<br/> (Geerbt von **CertificateICertificate2**)                          |
| [**Serialnumber**](certificate-serialnumber.md)<br/>   | Schreibgeschützt<br/>  | Ruft eine Zeichenfolge ab, die die Seriennummer des Zertifikats enthält.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                 |
| [**SubjectName**](certificate-subjectname.md)<br/>     | Schreibgeschützt<br/>  | Ruft eine Zeichenfolge ab, die den Namen des Zertifikatsubjekts enthält.<br/> (Geerbt von **CertificateICertificate2ICertificate**)           |
| [**Fingerabdruck**](certificate-thumbprint.md)<br/>       | Schreibgeschützt<br/>  | Ruft eine hexadezimale Zeichenfolge ab, die den SHA-1-Hash des Zertifikats enthält.<br/> (Geerbt von **CertificateICertificate2ICertificate**) |
| [**ValidFromDate**](certificate-validfromdate.md)<br/> | Schreibgeschützt<br/>  | Ruft das Anfangsdatum für die Gültigkeit des Zertifikats ab.<br/> (Geerbt von **CertificateICertificate2ICertificate**)               |
| [**ValidToDate**](certificate-validtodate.md)<br/>     | Schreibgeschützt<br/>  | Ruft das Enddatum für die Gültigkeit des Zertifikats ab.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                  |
| [**Version**](certificate-version.md)<br/>             | Schreibgeschützt<br/>  | Ruft die Versionsnummer des Zertifikats ab.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                |



 

## <a name="remarks"></a>Hinweise

Das **Certificate-Objekt** kann erstellt werden und ist für Skripts sicher. Die ProgID für das **Certificate-Objekt** lautet "CAPICOM. Certificate.2".

**CAPICOM 1. *x*:** Die ProgID für das **Certificate-Objekt** ist "CAPICOM. Certificate.1".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
