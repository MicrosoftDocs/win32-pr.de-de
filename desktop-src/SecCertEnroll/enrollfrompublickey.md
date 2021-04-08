---
description: Initialisiert ein PKCS \# 10-Zertifikat Anforderungs Objekt, umschließt es in ein Objekt vom Typ "CMC Request", übermittelt die Anforderung "CMC" an eine Unternehmens Zertifizierungsstelle (Certification Authority, ca) und speichert das von der Zertifizierungsstelle zurückgegebene Zertifikat in einer Datei.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: Registrierungs frompublickey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752728"
---
# <a name="enrollfrompublickey"></a><span data-ttu-id="381fa-103">Registrierungs frompublickey</span><span class="sxs-lookup"><span data-stu-id="381fa-103">enrollFromPublicKey</span></span>

<span data-ttu-id="381fa-104">Das Registrierungs frompublickey-Beispiel Initialisiert ein PKCS \# 10-Zertifikat Anforderungs Objekt, umschließt es in ein Objekt vom Typ "CMC Request", sendet die Anforderung "CMC" an eine Unternehmens Zertifizierungsstelle (Certification Authority, ca) und speichert das von der Zertifizierungsstelle zurückgegebene Zertifikat in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="381fa-104">The enrollFromPublicKey sample initializes a PKCS \#10 certificate request object, wraps it in a CMC request object, submits the CMC request to an enterprise certification authority (CA), and saves the certificate returned by the CA in a file.</span></span>

## <a name="location"></a><span data-ttu-id="381fa-105">Standort</span><span class="sxs-lookup"><span data-stu-id="381fa-105">Location</span></span>

<span data-ttu-id="381fa-106">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner " *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC Registrierungs \\ frompublickey" installiert.</span><span class="sxs-lookup"><span data-stu-id="381fa-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollFromPublicKey folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="381fa-107">Diskussion</span><span class="sxs-lookup"><span data-stu-id="381fa-107">Discussion</span></span>

<span data-ttu-id="381fa-108">Das Beispiel "anmelfrompublickey":</span><span class="sxs-lookup"><span data-stu-id="381fa-108">The enrollFromPublicKey sample:</span></span>

1.  <span data-ttu-id="381fa-109">Verarbeitet die folgenden Befehlszeilenargumente:</span><span class="sxs-lookup"><span data-stu-id="381fa-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="381fa-110">Der Name einer Zertifikat Vorlage.</span><span class="sxs-lookup"><span data-stu-id="381fa-110">The name of a certificate template.</span></span>
    -   <span data-ttu-id="381fa-111">Der Name einer Datei, in der das installierte Zertifikat als Base64-codiertes Bytearray gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="381fa-111">The name of a file in which to save the installed certificate as a base64-encoded byte array.</span></span>
    -   <span data-ttu-id="381fa-112">Ein optionaler Name der Signaturzertifikat Vorlage.</span><span class="sxs-lookup"><span data-stu-id="381fa-112">An optional signing certificate template name.</span></span> <span data-ttu-id="381fa-113">Die Vorlage wird verwendet, um ein Signaturzertifikat zu erstellen, wenn keine im Zertifikat Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="381fa-113">The template is used to create a signing certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="381fa-114">Erstellt ein privates [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Schlüsselobjekt und ruft die [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) -Methode auf, um mithilfe des standardmäßigen Kryptografieanbieters, der Schlüsselgröße und der [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) -Werte für den aktuellen Computer einen asymmetrischen privaten Schlüssel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="381fa-114">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) private key object and calls the [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) method to create an asymmetric private key using the default cryptographic provider, key size, and [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) values for the current computer.</span></span>
3.  <span data-ttu-id="381fa-115">Ruft den Teil des öffentlichen Schlüssels des [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="381fa-115">Retrieves the public key portion of the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object.</span></span>
4.  <span data-ttu-id="381fa-116">Erstellt ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt und initialisiert es mit der in der Befehlszeile angegebenen Vorlage und dem öffentlichen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="381fa-116">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the template specified on the command line and the public key.</span></span>
5.  <span data-ttu-id="381fa-117">Erstellt ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt und initialisiert es mit dem PKCS \# 10-Anforderungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="381fa-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object.</span></span>
6.  <span data-ttu-id="381fa-118">Ruft ein vorhandenes Signaturzertifikat ab. wenn es nicht gefunden werden kann, wird von der in der Befehlszeile angegebenen Vorlage eine Zertifikat Anforderung erstellt, und es wird versucht, Sie zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="381fa-118">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="381fa-119">Findcertbykeyusage ist in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="381fa-119">The findCertByKeyUsage is defined in enrollCommon.cpp.</span></span>
7.  <span data-ttu-id="381fa-120">Überprüft die Zertifikat Kette.</span><span class="sxs-lookup"><span data-stu-id="381fa-120">Verifies the certificate chain.</span></span>
8.  <span data-ttu-id="381fa-121">Erstellt ein [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) -Objekt, initialisiert es mit dem Signaturzertifikat, ruft die [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) -Auflistung aus dem Objekt der CMC-Anforderung ab und fügt das Signaturzertifikat Objekt der Auflistung hinzu.</span><span class="sxs-lookup"><span data-stu-id="381fa-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the signing certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the signing certificate object to the collection.</span></span>
9.  <span data-ttu-id="381fa-122">Codiert die CMC-Anforderung mithilfe von [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).</span><span class="sxs-lookup"><span data-stu-id="381fa-122">Encodes the CMC request by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
10. <span data-ttu-id="381fa-123">Erstellt ein [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) -Objekt und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellen Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="381fa-123">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
11. <span data-ttu-id="381fa-124">Erstellt ein CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) -Objekt und verwendet es sowie die Zeichen folgen, die die Zertifizierungsstellen Konfiguration enthalten, und die Zertifikat Anforderung zum übermitteln der Anforderung an die Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="381fa-124">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
12. <span data-ttu-id="381fa-125">Hiermit wird der Status des Registrierungsprozesses überprüft und das installierte Zertifikat in einer Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="381fa-125">Checks the status of the enrollment process and saves the installed certificate to a file.</span></span> <span data-ttu-id="381fa-126">Die encodedefilew-Funktion ist in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="381fa-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="381fa-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="381fa-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="381fa-128">CMC-Anforderung</span><span class="sxs-lookup"><span data-stu-id="381fa-128">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="381fa-129">PKCS \# 10-Anforderung</span><span class="sxs-lookup"><span data-stu-id="381fa-129">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="381fa-130">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="381fa-130">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
