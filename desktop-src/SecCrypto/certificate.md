---
description: Stellt ein einzelnes digitales Zertifikat dar.
ms.assetid: da95312b-cc9f-44f0-9517-0b28c5fcfb61
title: Zertifikat Objekt
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
ms.openlocfilehash: 1360b197f0d7f5e0579a5378a37047e6a117a9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371114"
---
# <a name="certificate-object"></a>Zertifikat Objekt

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]

Das **Zertifikat** Objekt stellt ein einzelnes [*digitales Zertifikat*](../secgloss/d-gly.md)dar.

Das **Certificate** -Objekt macht die folgenden Schnittstellen verfügbar:

-   **ICertificate** – eingeführt in CAPICOM 1,0.
-   **ICertificate2** – eingeführt in CAPICOM 2,0.

## <a name="when-to-use"></a>Verwendung

Das **Zertifikat** Objekt wird verwendet, um die folgenden Aufgaben auszuführen:

-   Laden Sie Zertifikat Daten, einschließlich des privaten Schlüssels, aus einer Datei.
-   Informationen aus dem Zertifikat erhalten.
-   Gibt grundlegende Einschränkungen, EKU, erweiterte Eigenschaften, Erweiterungen, Schlüssel Verwendung, öffentlichen Schlüssel und Vorlagen Objekte zurück, die dem Zertifikat zugeordnet sind.
-   Bestimmen Sie, ob das Zertifikat gültig ist, und überprüfen Sie die Zugriffs Verfügbarkeit des privaten Schlüssels des Zertifikat Antragstellers.
-   Zeigen Sie das Zertifikat an.
-   Importieren und exportieren Sie das Zertifikat.
-   Speichern Sie das Zertifikat in einer Datei.
-   Ruft Eigenschaften ab, die das Zertifikat beschreiben, oder legt diese fest.

## <a name="members"></a>Member

Das **Zertifikat** Objekt enthält diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Zertifikat** Objekt verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Basiceinschränkungen**](certificate-basicconstraints.md)     | Gibt ein [**basiceinschränkungs**](basicconstraints.md) -Objekt zurück, das die grundlegende Einschränkungs Erweiterung des Zertifikats darstellt.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                   |
| [**Ausgestellten**](certificate-display.md)                       | Zeigt ein Zertifikat an.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                                                                                                                             |
| [**Exportieren**](certificate-export.md)                         | Kopiert ein Zertifikat in eine codierte Zeichenfolge. Die codierte Zeichenfolge kann in eine Datei geschrieben oder in ein neues **Zertifikat** Objekt importiert werden.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                               |
| [**Extendedkeyusage**](certificate-extendedkeyusage.md)     | Gibt ein [**extendedkeyusage**](extendedkeyusage.md) -Objekt zurück, das die gültige erweiterte Schlüssel Verwendung des Zertifikats angibt.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                       |
| [**ExtendedProperties**](certificate-extendedproperties.md) | Gibt eine Auflistung der erweiterten Eigenschaften des Zertifikats zurück.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                             |
| [**Erweiterungen**](certificate-extensions.md)                 | Gibt eine Auflistung der Erweiterungen zurück, die dem Zertifikat zugeordnet sind.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                         |
| [**GetInfo**](certificate-getinfo.md)                       | Ruft Informationen aus dem Zertifikat ab.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                                                                                                         |
| [**HasPrivateKey**](certificate-hasprivatekey.md)           | Bestimmt, ob dem Zertifikat ein [*privater Schlüssel*](../secgloss/p-gly.md) zugeordnet ist.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                    |
| [**Importieren**](certificate-import.md)                         | Importiert ein zuvor codiertes Zertifikat aus einer Zeichenfolge in das **Zertifikat** Objekt.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                                                             |
| [**IsValid**](certificate-isvalid.md)                       | Erstellt eine Zertifikat Überprüfungs Kette für ein Zertifikat und gibt ein [**CertificateStatus**](certificatestatus.md) -Objekt zurück, das den Gültigkeits Status des Zertifikats enthält.<br/> (Geerbt von **CertificateICertificate2ICertificate**) |
| [**Endeinheits Zertifikaten der**](certificate-keyusage.md)                     | Gibt ein [**KeyUsage**](keyusage.md) -Objekt zurück, das die gültige Schlüssel Verwendung des Zertifikats angibt.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                                                                |
| [**Laden**](certificate-load.md)                             | Importiert ein Zertifikat aus einer Datei.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                                                              |
| [**PublicKey**](certificate-publickey.md)                   | Gibt ein [**PublicKey**](publickey.md) -Objekt zurück.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                                                |
| [**Speichern**](certificate-save.md)                             | Speichert das Zertifikat in einer Datei.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                                                                |
| [**Vorlage**](certificate-template.md)                     | Gibt die Vorlage zurück, die dem Zertifikat zugeordnet ist.<br/> (Geerbt von **CertificateICertificate2**)                                                                                                                                           |



 

### <a name="properties"></a>Eigenschaften

Das **Zertifikat** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp           | BESCHREIBUNG                                                                                                                                          |
|:--------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Archiviert**](certificate-archived.md)<br/>           | Lesen/Schreiben<br/> | Legt einen booleschen Wert fest, der angibt, ob das Zertifikat archiviert ist, oder ruft diesen ab.<br/> (Geerbt von **CertificateICertificate2**)       |
| [**IssuerName**](certificate-issuername.md)<br/>       | Schreibgeschützt<br/>  | Ruft eine Zeichenfolge ab, die den Namen des Zertifikat Ausstellers enthält.<br/> (Geerbt von **CertificateICertificate2ICertificate**)            |
| [**PrivateKey**](certificate-privatekey.md)<br/>       | Lesen/Schreiben<br/> | Legt den privaten Schlüssel fest, der dem Zertifikat zugeordnet ist, oder ruft ihn ab.<br/> (Geerbt von **CertificateICertificate2**)                          |
| [**SerialNumber**](certificate-serialnumber.md)<br/>   | Schreibgeschützt<br/>  | Ruft eine Zeichenfolge ab, die die Seriennummer des Zertifikats enthält.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                 |
| [**SubjectName**](certificate-subjectname.md)<br/>     | Schreibgeschützt<br/>  | Ruft eine Zeichenfolge ab, die den Namen des Zertifikat Antragstellers enthält.<br/> (Geerbt von **CertificateICertificate2ICertificate**)           |
| [**Fingerabdruck**](certificate-thumbprint.md)<br/>       | Schreibgeschützt<br/>  | Ruft eine hexadezimale Zeichenfolge ab, die den SHA-1-Hash des Zertifikats enthält.<br/> (Geerbt von **CertificateICertificate2ICertificate**) |
| [**Validfromdate**](certificate-validfromdate.md)<br/> | Schreibgeschützt<br/>  | Ruft das Anfangsdatum für die Gültigkeit des Zertifikats ab.<br/> (Geerbt von **CertificateICertificate2ICertificate**)               |
| [**Validdate**](certificate-validtodate.md)<br/>     | Schreibgeschützt<br/>  | Ruft das Enddatum für die Gültigkeit des Zertifikats ab.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                  |
| [**Version**](certificate-version.md)<br/>             | Schreibgeschützt<br/>  | Ruft die Versionsnummer des Zertifikats ab.<br/> (Geerbt von **CertificateICertificate2ICertificate**)                                |



 

## <a name="remarks"></a>Bemerkungen

Das **Zertifikat** Objekt kann erstellt werden und ist für die Skripterstellung sicher. Die ProgID für das **Zertifikat** Objekt ist "CAPICOM". Zertifikat. 2 ".

**CAPICOM 1. *x*:** die ProgID für das **Zertifikat** Objekt ist "CAPICOM". Zertifikat. 1 ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------------|----------------------------------------------------------------------------------------|
| Ende des Supports (Client)<br/> | Windows Vista<br/>                                                               |
| Ende des Supports (Server)<br/> | Windows Server 2008<br/>                                                         |
| Verteilbare Komponente<br/>       | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
