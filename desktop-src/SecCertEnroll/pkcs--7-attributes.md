---
description: PKCS \# 7 ist ein Kryptografienachrichtensyntaxstandard.
ms.assetid: fd4e2a13-f257-4ba9-a11d-35f49c5a6c00
title: PKCS \# 7-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24436a918afe2d9bd85d7c28ae330b8c022bd4e3d34d30e58aae7b9c57c4963a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774585"
---
# <a name="pkcs-7-attributes"></a>PKCS \# 7-Attribute

PKCS \# 7 ist ein Kryptografienachrichtensyntaxstandard. Eine PKCS \# 7-Nachricht stellt allein keine Zertifikatanforderung dar, kann aber eine PKCS \# 10- oder CMC-Anforderung in einer **ContentInfo** ASN.1-Struktur mit einem der folgenden Inhaltstypen kapseln. Mit der Kapselung können Sie zusätzliche Funktionen wie mehrere Signaturen hinzufügen, die andernfalls nicht verfügbar sind.

-   **Daten**
-   **SignedData**
-   **EnvelopedData**
-   **SignedAndEnvelopedData**
-   **DigestedData**
-   **Encrypteddata**

Attribute können den Feldern **authenticatedAttributes** und **unauthenticatedAttributes** des **SignedData-Inhaltstyps** hinzugefügt werden.

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

Der Prozess, der zum Archivieren des privaten Schlüssels eines Clients bei einer Zertifizierungsstelle erforderlich ist, bietet ein umfassendes Beispiel dafür, wie authentifizierte (signierte) Attribute und die nicht authentifizierten Attribute verwendet werden können:

-   Der Client erstellt ein [**IX509CertificateRequestPkcs10-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) und fügt geeignete Daten für den angeforderten Zertifikattyp hinzu.
-   Der Client verwendet die PKCS \# 10-Anforderung, um ein [**IX509CertificateRequestCmc-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) zu initialisieren. Die PKCS \# 10-Anforderung wird in der CMC-Anforderung in der **TaggedRequest-Struktur** platziert. Weitere Informationen finden Sie unter [CMC-Attribute.](cmc-attributes.md)
-   Der Client verschlüsselt einen privaten Schlüssel und verwendet ihn, um ein [**IX509AttributeArchiveKey-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) zu initialisieren. Das neue **ArchiveKey-Attribut** wird in einer **EnvelopedData-Struktur** gekapselt.

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

-   Der Client erstellt einen SHA-1-Hash des verschlüsselten Schlüssels und verwendet ihn zum Initialisieren eines [**IX509AttributeArchiveKeyHash-Objekts.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)
-   Der Client ruft die [**CryptAttributes-Auflistung**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) aus der CMC-Anforderung ab und fügt ihr die Attribute **ArchiveKey** und **ArchiveKeyHash** hinzu. Die Attribute werden in der **TaggedAttributes-Struktur** der CMC-Anforderung platziert.
-   Der Client verwendet die CMC-Anforderung, um ein [**IX509CertificateRequestPkcs7-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) zu initialisieren. Dadurch wird die CMC-Anforderung in das **contentInfo-Feld** der PKCS \# 7 **SignedData-Struktur** eingefügt.
-   Das **ArchiveKeyHash-Attribut** wird signiert und in der **authenticatedAttributes-Sequenz** der **SignerInfo-Struktur** platziert.
-   Das **ArchiveKey-Attribut** wird in der **Sequenz unauthenticatedAttributes** der **SignerInfo-Struktur platziert,** die dem primären Signierer der PKCS \# 7-Nachricht zugeordnet ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützte Attribute](supported-attributes.md)
</dt> </dl>

 

 



