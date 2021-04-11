---
description: Liest eine vorhandene CMC-Zertifikat Anforderung aus einer Datei, umschließt Sie in eine andere CMC-Anforderung, signiert diese äußere Anforderung, sendet Sie an eine Zertifizierungsstelle (Certification Authority, ca) und speichert die Zertifikats Antwort von der Zertifizierungsstelle in einer Datei.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: registrinetstedcmc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1df25a1bc7f6ce16a67f66ff58dc371a526813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214404"
---
# <a name="enrollnestedcmc"></a><span data-ttu-id="e2b64-103">registrinetstedcmc</span><span class="sxs-lookup"><span data-stu-id="e2b64-103">enrollNestedCMC</span></span>

<span data-ttu-id="e2b64-104">Das Beispiel "registrinetstedcmc" liest eine vorhandene CMC-Zertifikat Anforderung aus einer Datei, umschließt Sie in eine andere CMC-Anforderung, signiert diese äußere Anforderung, sendet Sie an eine Zertifizierungsstelle (Certification Authority, ca) und speichert die Zertifikats Antwort von der Zertifizierungsstelle in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="e2b64-104">The enrollNestedCMC sample reads an existing CMC certificate request from a file, wraps it in another CMC request, signs this outer request, submits it to a certification authority (CA), and saves the certificate response from the CA to a file.</span></span>

## <a name="location"></a><span data-ttu-id="e2b64-105">Standort</span><span class="sxs-lookup"><span data-stu-id="e2b64-105">Location</span></span>

<span data-ttu-id="e2b64-106">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ X509 Certificate registriment \\ VC \\ registrierungsregistrierungs Ordner installiert.</span><span class="sxs-lookup"><span data-stu-id="e2b64-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\VC\\enrollNestedCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="e2b64-107">Diskussion</span><span class="sxs-lookup"><span data-stu-id="e2b64-107">Discussion</span></span>

<span data-ttu-id="e2b64-108">Das Beispiel "registrinetstedcmc":</span><span class="sxs-lookup"><span data-stu-id="e2b64-108">The enrollNestedCMC sample:</span></span>

1.  <span data-ttu-id="e2b64-109">Verarbeitet die folgenden Befehlszeilenargumente:</span><span class="sxs-lookup"><span data-stu-id="e2b64-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="e2b64-110">Der Name der Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="e2b64-110">The name of the input file.</span></span>
    -   <span data-ttu-id="e2b64-111">Der Name der Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="e2b64-111">The name of the output file.</span></span>
    -   <span data-ttu-id="e2b64-112">Eine optionale Anforderungs Vorlage.</span><span class="sxs-lookup"><span data-stu-id="e2b64-112">An optional request template.</span></span>
2.  <span data-ttu-id="e2b64-113">Liest eine vorhandene CMC-Anforderung aus einer Datei als base63-codiertes Bytearray, konvertiert das Bytearray in ein **BSTR**, erstellt ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt und verwendet **BSTR** , um das Anforderungs Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="e2b64-113">Reads an existing CMC request from a file as a base63-encoded byte array, converts the byte array to a **BSTR**, creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object, and uses the **BSTR** to initialize the request object.</span></span> <span data-ttu-id="e2b64-114">Das initialisierte-Objekt wird zum inneren Request.</span><span class="sxs-lookup"><span data-stu-id="e2b64-114">The initialized object becomes the inner request.</span></span>
3.  <span data-ttu-id="e2b64-115">Verwendet das interne Anforderungs Objekt, das im vorherigen Schritt erstellt und initialisiert wurde, um eine andere CMC-Anforderung zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="e2b64-115">Uses the inner request object created and initialized in the preceding step to initialize another CMC request.</span></span>
4.  <span data-ttu-id="e2b64-116">Ruft ein vorhandenes Signaturzertifikat ab. wenn es nicht gefunden werden kann, wird von der in der Befehlszeile angegebenen Vorlage eine Zertifikat Anforderung erstellt, und es wird versucht, Sie zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e2b64-116">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="e2b64-117">Die Funktionen "findcertbytemplate" und "registricertbytemplate" sind in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="e2b64-117">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
5.  <span data-ttu-id="e2b64-118">Ruft die [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) -Auflistung aus der äußeren CMC-Anforderung ab, erstellt ein neues [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) -Objekt, initialisiert es mit dem abgerufenen Signaturzertifikat und fügt es der Auflistung hinzu.</span><span class="sxs-lookup"><span data-stu-id="e2b64-118">Retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the outer CMC request, creates a new [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the retrieved signing certificate, and adds it to the collection.</span></span>
6.  <span data-ttu-id="e2b64-119">Codiert die CMC-Anforderung mithilfe von Distinguished Encoding Rules (der) und ruft die Anforderung als **BSTR** ab.</span><span class="sxs-lookup"><span data-stu-id="e2b64-119">Encodes the CMC request by using Distinguished Encoding Rules (DER) and retrieves the request as a **BSTR**.</span></span>
7.  <span data-ttu-id="e2b64-120">Erstellt ein [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) -Objekt und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellen Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="e2b64-120">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
8.  <span data-ttu-id="e2b64-121">Erstellt ein CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) -Objekt und verwendet es sowie die Zeichen folgen, die die Zertifizierungsstellen Konfiguration enthalten, und die Zertifikat Anforderung zum übermitteln der Anforderung an die Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="e2b64-121">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
9.  <span data-ttu-id="e2b64-122">Hiermit wird der Status des Registrierungsprozesses überprüft und die Zertifikats Antwort der Zertifizierungsstelle in einer Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e2b64-122">Checks the status of the enrollment process and saves the certificate response from the CA to a file.</span></span> <span data-ttu-id="e2b64-123">Die encodedefilew-Funktion ist in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="e2b64-123">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2b64-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2b64-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2b64-125">CMC-Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2b64-125">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="e2b64-126">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2b64-126">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
