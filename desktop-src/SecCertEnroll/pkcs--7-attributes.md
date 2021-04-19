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
# <a name="pkcs-7-attributes"></a><span data-ttu-id="b7046-103">PKCS \# 7-Attribute</span><span class="sxs-lookup"><span data-stu-id="b7046-103">PKCS \#7 Attributes</span></span>

<span data-ttu-id="b7046-104">PKCS \# 7 ist ein kryptografischer Nachrichten Syntax Standard.</span><span class="sxs-lookup"><span data-stu-id="b7046-104">PKCS \#7 is a cryptographic message syntax standard.</span></span> <span data-ttu-id="b7046-105">Eine PKCS \# 7-Nachricht stellt nicht allein eine Zertifikat Anforderung dar, Sie kann jedoch eine PKCS 10-oder eine \# CMC-Anforderung in einer **ContentInfo** -ASN. 1-Struktur mithilfe eines der folgenden Inhaltstypen Kapseln.</span><span class="sxs-lookup"><span data-stu-id="b7046-105">A PKCS \#7 message does not, by itself, constitute a certificate request, but it can encapsulate a PKCS \#10 or CMC request in a **ContentInfo** ASN.1 structure by using one of the following content types.</span></span> <span data-ttu-id="b7046-106">Mithilfe der Kapselung können Sie zusätzliche Funktionen hinzufügen, z. b. mehrere Signaturen, die ansonsten nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b7046-106">Encapsulation enables you to add extra functionality, such as multiple signatures, that is not otherwise available.</span></span>

-   <span data-ttu-id="b7046-107">**Daten**</span><span class="sxs-lookup"><span data-stu-id="b7046-107">**Data**</span></span>
-   <span data-ttu-id="b7046-108">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="b7046-108">**SignedData**</span></span>
-   <span data-ttu-id="b7046-109">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="b7046-109">**EnvelopedData**</span></span>
-   <span data-ttu-id="b7046-110">**Signetzdandenvelopeddata**</span><span class="sxs-lookup"><span data-stu-id="b7046-110">**SignedAndEnvelopedData**</span></span>
-   <span data-ttu-id="b7046-111">**DigestedData**</span><span class="sxs-lookup"><span data-stu-id="b7046-111">**DigestedData**</span></span>
-   <span data-ttu-id="b7046-112">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="b7046-112">**EncryptedData**</span></span>

<span data-ttu-id="b7046-113">Attribute können den Feldern " **authenticatedattributes** " und " **unauthenticatedattributes** " des Inhaltstyps " **SignedData** " hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b7046-113">Attributes can be added to the **authenticatedAttributes** and **unauthenticatedAttributes** fields of the **SignedData** content type.</span></span>

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

<span data-ttu-id="b7046-114">Der Prozess, der zum Archivieren des privaten Schlüssels eines Clients auf einer Zertifizierungsstelle (Certification Authority, ca) erforderlich ist, bietet ein umfassendes Beispiel dafür, wie authentifizierte (signierte) Attribute und die nicht authentifizierten Attribute verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="b7046-114">The process required to archive a client's private key on a certification authority (CA) provides a comprehensive example of how authenticated (signed) attributes and the unauthenticated attributes can be used:</span></span>

-   <span data-ttu-id="b7046-115">Der Client erstellt ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt und fügt geeignete Daten für den angeforderten Zertifikattyp hinzu.</span><span class="sxs-lookup"><span data-stu-id="b7046-115">The client creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and adds appropriate data for the type of certificate being requested.</span></span>
-   <span data-ttu-id="b7046-116">Der Client verwendet die PKCS \# 10-Anforderung, um ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b7046-116">The client uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span> <span data-ttu-id="b7046-117">Die PKCS \# 10-Anforderung wird in die " **taggedrequest** "-Struktur in der CMC-Anforderung eingefügt.</span><span class="sxs-lookup"><span data-stu-id="b7046-117">The PKCS \#10 request is placed into the **TaggedRequest** structure in the CMC request.</span></span> <span data-ttu-id="b7046-118">Weitere Informationen finden Sie unter [CMC-Attribute](cmc-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b7046-118">For more information, see [CMC Attributes](cmc-attributes.md).</span></span>
-   <span data-ttu-id="b7046-119">Der Client verschlüsselt einen privaten Schlüssel und verwendet ihn, um ein [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) -Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b7046-119">The client encrypts a private key and uses it to initialize an [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) object.</span></span> <span data-ttu-id="b7046-120">Das neue **archivekey** -Attribut ist in einer **EnvelopedData** -Struktur gekapselt.</span><span class="sxs-lookup"><span data-stu-id="b7046-120">The new **ArchiveKey** attribute is encapsulated in an **EnvelopedData** structure.</span></span>

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

-   <span data-ttu-id="b7046-121">Der Client erstellt einen SHA-1-Hash des verschlüsselten Schlüssels und verwendet ihn, um ein [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) -Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b7046-121">The client creates a SHA-1 hash of the encrypted key and uses it to initialize an [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) object.</span></span>
-   <span data-ttu-id="b7046-122">Der Client ruft die [**cryptattributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) -Auflistung von der CMC-Anforderung ab und fügt ihm das **archivekey** -Attribut und das **archivekeyhash** -Attribut hinzu.</span><span class="sxs-lookup"><span data-stu-id="b7046-122">The client retrieves the [**CryptAttributes**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_cryptattributes) collection from the CMC request and adds the **ArchiveKey** and the **ArchiveKeyHash** attributes to it.</span></span> <span data-ttu-id="b7046-123">Die Attribute werden in die **taggedattributes** -Struktur der CMC-Anforderung eingefügt.</span><span class="sxs-lookup"><span data-stu-id="b7046-123">The attributes are placed into the **TaggedAttributes** structure of the CMC request.</span></span>
-   <span data-ttu-id="b7046-124">Der Client verwendet die CMC-Anforderung, um ein [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) -Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b7046-124">The client uses the CMC request to initialize an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object.</span></span> <span data-ttu-id="b7046-125">Dadurch wird die CMC-Anforderung in das **ContentInfo** -Feld der "PKCS \# 7 **SignedData** "-Struktur eingefügt.</span><span class="sxs-lookup"><span data-stu-id="b7046-125">This places the CMC request into the **contentInfo** field of the PKCS \#7 **SignedData** structure.</span></span>
-   <span data-ttu-id="b7046-126">Das **archivekeyhash** -Attribut wird signiert und in der **authenticatedattributes** -Sequenz der **SignerInfo** -Struktur abgelegt.</span><span class="sxs-lookup"><span data-stu-id="b7046-126">The **ArchiveKeyHash** attribute is signed and placed in the **authenticatedAttributes** sequence of the **SignerInfo** structure.</span></span>
-   <span data-ttu-id="b7046-127">Das **archivekey** -Attribut wird in der **unauthenticatedattributes** -Sequenz der **SignerInfo** -Struktur platziert, die dem primären Signatur Geber der PKCS 7-Meldung zugeordnet ist \# .</span><span class="sxs-lookup"><span data-stu-id="b7046-127">The **ArchiveKey** attribute is placed in the **unauthenticatedAttributes** sequence of the **SignerInfo** structure associated with the primary signer of the PKCS \#7 message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7046-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b7046-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7046-129">Unterstützte Attribute</span><span class="sxs-lookup"><span data-stu-id="b7046-129">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



