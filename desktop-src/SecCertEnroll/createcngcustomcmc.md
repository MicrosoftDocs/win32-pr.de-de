---
description: Erstellt ein Objekt vom Objekt "CMC Request" aus einer inneren geschachtelten PKCS \# 10-Anforderung.
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: "\"kreatecngcustomcmc\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342729"
---
# <a name="createcngcustomcmc"></a><span data-ttu-id="6e6fb-103">"kreatecngcustomcmc"</span><span class="sxs-lookup"><span data-stu-id="6e6fb-103">createCNGCustomCMC</span></span>

<span data-ttu-id="6e6fb-104">Das Beispiel "samatecngcustomcmc" erstellt ein Objekt vom Objekt "CMC Request" aus einer inneren geschachtelten PKCS \# 10-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-104">The createCNGCustomCMC sample creates a CMC request object from an inner nested PKCS \#10 request.</span></span> <span data-ttu-id="6e6fb-105">Die innere Anforderung wird mit einem asymmetrischen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly)erstellt.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-105">The inner request is created by using an asymmetric [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="6e6fb-106">Der private Schlüssel wird mit dem Kryptografieanbieter Cryptography API: Next Generation (CNG) und dem in der Befehlszeile angegebenen Algorithmus erstellt.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-106">The private key is created by using the Cryptography API: Next Generation (CNG) cryptographic provider and the algorithm specified on the command line.</span></span> <span data-ttu-id="6e6fb-107">Außerdem werden benutzerdefinierte Optionen wie Export Richtlinie und Schlüsselschutz Ebene für den privaten Schlüssel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-107">Custom options such as export policy and key protection level are also set on the private key.</span></span>

## <a name="location"></a><span data-ttu-id="6e6fb-108">Standort</span><span class="sxs-lookup"><span data-stu-id="6e6fb-108">Location</span></span>

<span data-ttu-id="6e6fb-109">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC | \\ atecngcustomcmc installiert.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-109">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\createCNGCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="6e6fb-110">Diskussion</span><span class="sxs-lookup"><span data-stu-id="6e6fb-110">Discussion</span></span>

<span data-ttu-id="6e6fb-111">Das Beispiel "samatecngcustomcmc":</span><span class="sxs-lookup"><span data-stu-id="6e6fb-111">The createCNGCustomCMC sample:</span></span>

1.  <span data-ttu-id="6e6fb-112">Verarbeitet die folgenden Befehlszeilenargumente:</span><span class="sxs-lookup"><span data-stu-id="6e6fb-112">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="6e6fb-113">Der Name eines CNG- [*Kryptografiedienstanbieters*](/windows/desktop/SecGloss/c-gly) (CSP).</span><span class="sxs-lookup"><span data-stu-id="6e6fb-113">The name of a CNG [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span>
    -   <span data-ttu-id="6e6fb-114">Der Name des Algorithmus, der verwendet wird, um einen asymmetrischen privaten Schlüssel zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-114">The name of the algorithm used to generate an asymmetric private key.</span></span>
    -   <span data-ttu-id="6e6fb-115">Der Name des Algorithmus, der zum [*Hash*](/windows/desktop/SecGloss/h-gly) der [*Zertifikat Anforderung*](/windows/desktop/SecGloss/c-gly)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-115">The name of the algorithm used to [*hash*](/windows/desktop/SecGloss/h-gly) the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>
    -   <span data-ttu-id="6e6fb-116">Eine Ausgabedatei, in der die Zertifikat Anforderung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-116">An output file in which to save the certificate request.</span></span>
    -   <span data-ttu-id="6e6fb-117">Eine optionale Zeichenfolge (Alternative Signatur), die, falls vorhanden, angibt, dass ein diskreter anstelle eines kombinierten Signatur Algorithmus verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-117">An optional string (AlternateSignature) which, if present, specifies that a discrete rather than a combined signature algorithm be used.</span></span> <span data-ttu-id="6e6fb-118">Weitere Informationen finden Sie unter der Eigenschaft " [**Alternative**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) Eigenschaft".</span><span class="sxs-lookup"><span data-stu-id="6e6fb-118">For more information, see the [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) property.</span></span>
2.  <span data-ttu-id="6e6fb-119">Erstellt ein [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt und legt die folgenden Eigenschaften fest:</span><span class="sxs-lookup"><span data-stu-id="6e6fb-119">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object and sets the following properties:</span></span>
    -   [<span data-ttu-id="6e6fb-120">**Legacycsp**</span><span class="sxs-lookup"><span data-stu-id="6e6fb-120">**LegacyCsp**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [<span data-ttu-id="6e6fb-121">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="6e6fb-121">**ProviderName**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [<span data-ttu-id="6e6fb-122">**Algorithmus**</span><span class="sxs-lookup"><span data-stu-id="6e6fb-122">**Algorithm**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [<span data-ttu-id="6e6fb-123">**Keyprotection**</span><span class="sxs-lookup"><span data-stu-id="6e6fb-123">**KeyProtection**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [<span data-ttu-id="6e6fb-124">**ExportPolicy**</span><span class="sxs-lookup"><span data-stu-id="6e6fb-124">**ExportPolicy**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  <span data-ttu-id="6e6fb-125">Erstellt einen asymmetrischen privaten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-125">Creates an asymmetric private key.</span></span>
4.  <span data-ttu-id="6e6fb-126">Erstellt ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt und initialisiert es mit dem privaten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-126">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the private key.</span></span>
5.  <span data-ttu-id="6e6fb-127">Erstellt ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt und initialisiert es mit dem \# in Schritt 4 erstellten PKCS 10-Anforderungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-127">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object created in step 4.</span></span>
6.  <span data-ttu-id="6e6fb-128">Legt das Flag für den alternativen Signatur Algorithmus auf **Variant \_ true** oder **Variant \_ false** fest, je nachdem, ob eine Alternative Signatur Zeichenfolge in der Befehlszeile angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-128">Sets the alternate signature algorithm flag to **VARIANT\_TRUE** or **VARIANT\_FALSE** depending on whether an alternate signature string is specified on the command line.</span></span> <span data-ttu-id="6e6fb-129">Weitere Informationen finden Sie unter " [**Alternative**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm)zu".</span><span class="sxs-lookup"><span data-stu-id="6e6fb-129">For more information, see [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span></span>
7.  <span data-ttu-id="6e6fb-130">Erstellt eine [*Hash Algorithmus*](/windows/desktop/SecGloss/h-gly) - [*Objekt Kennung*](/windows/desktop/SecGloss/o-gly) (OID) aus dem Algorithmusnamen, der in der Befehlszeile angegeben ist, und legt die OID für das Objekt "CMC Request" fest.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-130">Creates a [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) from the algorithm name specified on the command line and sets the OID on the CMC request object.</span></span>
8.  <span data-ttu-id="6e6fb-131">Signiert die Zertifikat Anforderung und codiert Sie mithilfe von [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).</span><span class="sxs-lookup"><span data-stu-id="6e6fb-131">Signs the certificate request and encodes it by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
9.  <span data-ttu-id="6e6fb-132">Ruft eine Zeichenfolge ab, die die codierte CMC-Zertifikat Anforderung enthält, und speichert Sie in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-132">Retrieves a string that contains the encoded CMC certificate request and saves it to a file.</span></span> <span data-ttu-id="6e6fb-133">Die encodedefilew-Funktion ist in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="6e6fb-133">The EncodeToFileW function is defined in EnrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e6fb-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e6fb-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e6fb-135">CMC-Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e6fb-135">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="6e6fb-136">PKCS \# 10-Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e6fb-136">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="6e6fb-137">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e6fb-137">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> <dt>

[<span data-ttu-id="6e6fb-138">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="6e6fb-138">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
