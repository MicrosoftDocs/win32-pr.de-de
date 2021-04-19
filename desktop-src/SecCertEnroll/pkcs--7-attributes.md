---
description: PKCS \# 7 ist ein kryptografischer Nachrichten Syntax Standard.
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: PKCS \# 7-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0c7bc9b991a6625cae36ae9857275a9d86786a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362886"
---
# <a name="pkcs-7-attributes"></a>PKCS \# 7-Attribute

PKCS \# 7 ist ein kryptografischer Nachrichten Syntax Standard. Eine PKCS \# 7-Nachricht stellt nicht allein eine Zertifikat Anforderung dar, Sie kann jedoch eine PKCS 10-oder eine \# CMC-Anforderung in einer **ContentInfo** -ASN. 1-Struktur mithilfe eines der folgenden Inhaltstypen Kapseln. Mithilfe der Kapselung können Sie zusätzliche Funktionen hinzufügen, z. b. mehrere Signaturen, die ansonsten nicht verfügbar sind.

-   **Daten**
-   **SignedData**
-   **EnvelopedData**
-   **Signetzdandenvelopeddata**
-   **DigestedData**
-   **EncryptedData**

Attribute können den Feldern " **authenticatedattributes** " und " **unauthenticatedattributes** " des Inhaltstyps " **SignedData** " hinzugefügt werden.

``` syntax
SignedData ::= SEQUENCE 
{
   version             INTEGER,
   digestAlgorithms    DigestAlgorithmIdentifiers,
   contentInfo         ContentInfo,
   certificates        [0] IMPLICIT Certificates OPTIONAL,
   crls                [1] IMPLICIT CertificateRevocationLists OPTIONAL,
   signerInfos         SignerInfos
}

SignerInfos ::= SET OF SignerInfo

SignerInfo ::= SEQUENCE 
{
    version                     INTEGER,
    sid                         CertIdentifier,
    digestAlgorithm             DigestAlgorithmIdentifier,
    authenticatedAttributes     [0] IMPLICIT Attributes OPTIONAL,
    digestEncryptionAlgorithm   DigestEncryptionAlgId,
    encryptedDigest             EncryptedDigest,
    unauthenticatedAttributes   [1] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

Der Prozess, der zum Archivieren des privaten Schlüssels eines Clients auf einer Zertifizierungsstelle (Certification Authority, ca) erforderlich ist, bietet ein umfassendes Beispiel dafür, wie authentifizierte (signierte) Attribute und die nicht authentifizierten Attribute verwendet werden können:

-   Der Client erstellt ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt und fügt geeignete Daten für den angeforderten Zertifikattyp hinzu.
-   Der Client verwendet die PKCS \# 10-Anforderung, um ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt zu initialisieren. Die PKCS \# 10-Anforderung wird in die " **taggedrequest** "-Struktur in der CMC-Anforderung eingefügt. Weitere Informationen finden Sie unter [CMC-Attribute](cmc-attributes.md).
-   Der Client verschlüsselt einen privaten Schlüssel und verwendet ihn, um ein [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) -Objekt zu initialisieren. Das neue **archivekey** -Attribut ist in einer **EnvelopedData** -Struktur gekapselt.

    ``` syntax
    EnvelopedData ::= SEQUENCE 
    {
        version                 INTEGER,
        recipientInfos          RecipientInfos,
        encryptedContentInfo    EncryptedContentInfo
    } 

    RecipientInfos ::= SET OF RecipientInfo

    EncryptedContentInfo ::= SEQUENCE 
    {
        contentType                 ContentType,
        contentEncryptionAlgorithm  ContentEncryptionAlgId,
        encryptedContent            [0] IMPLICIT EncryptedContent OPTIONAL
    } 

    EncryptedContent ::= OCTET STRING

    RecipientInfo ::= SEQUENCE 
    {
        version                 INTEGER,
        issuerAndSerialNumber   IssuerAndSerialNumber,
        keyEncryptionAlgorithm  KeyEncryptionAlgId,
        encryptedKey            EncryptedKey
    } 
    ```

-   Der Client erstellt einen SHA-1-Hash des verschlüsselten Schlüssels und verwendet ihn, um ein [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) -Objekt zu initialisieren.
-   Der Client ruft die [**cryptattributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) -Auflistung von der CMC-Anforderung ab und fügt ihm das **archivekey** -Attribut und das **archivekeyhash** -Attribut hinzu. Die Attribute werden in die **taggedattributes** -Struktur der CMC-Anforderung eingefügt.
-   Der Client verwendet die CMC-Anforderung, um ein [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) -Objekt zu initialisieren. Dadurch wird die CMC-Anforderung in das **ContentInfo** -Feld der "PKCS \# 7 **SignedData** "-Struktur eingefügt.
-   Das **archivekeyhash** -Attribut wird signiert und in der **authenticatedattributes** -Sequenz der **SignerInfo** -Struktur abgelegt.
-   Das **archivekey** -Attribut wird in der **unauthenticatedattributes** -Sequenz der **SignerInfo** -Struktur platziert, die dem primären Signatur Geber der PKCS 7-Meldung zugeordnet ist \# .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützte Attribute](supported-attributes.md)
</dt> </dl>

 

 



