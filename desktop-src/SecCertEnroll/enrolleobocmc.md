---
description: Erstellt eine CMC-Zertifikat Anforderung im Auftrag eines anderen Benutzers und registriert den Benutzer in einer Zertifikatshierarchie.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: Einschreibung von "Einschreibung"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526993"
---
# <a name="enrolleobocmc"></a><span data-ttu-id="0157b-103">Einschreibung von "Einschreibung"</span><span class="sxs-lookup"><span data-stu-id="0157b-103">enrollEOBOCMC</span></span>

<span data-ttu-id="0157b-104">Das Ereignis "" "" "" "" "" "" "" ""</span><span class="sxs-lookup"><span data-stu-id="0157b-104">The enrollEOBOCMC sample creates a CMC certificate request on behalf of another user and enrolls the user in a certificate hierarchy.</span></span> <span data-ttu-id="0157b-105">Die Registrierung im Namen eines anderen Benutzers erfordert, dass die Zertifikat Anforderung mit einem Registrierungs-Agent-Zertifikat signiert wird.</span><span class="sxs-lookup"><span data-stu-id="0157b-105">Enrollment on behalf of another user requires that the certificate request be signed by using an enrollment agent certificate.</span></span>

## <a name="location"></a><span data-ttu-id="0157b-106">Standort</span><span class="sxs-lookup"><span data-stu-id="0157b-106">Location</span></span>

<span data-ttu-id="0157b-107">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC Einschreibung \\ leobocmc installiert.</span><span class="sxs-lookup"><span data-stu-id="0157b-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollEOBOCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="0157b-108">Diskussion</span><span class="sxs-lookup"><span data-stu-id="0157b-108">Discussion</span></span>

<span data-ttu-id="0157b-109">Das Beispiel "Einschreibung-obocmc":</span><span class="sxs-lookup"><span data-stu-id="0157b-109">The enrollEOBOCMC sample:</span></span>

1.  <span data-ttu-id="0157b-110">Verarbeitet die folgenden Befehlszeilenargumente:</span><span class="sxs-lookup"><span data-stu-id="0157b-110">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="0157b-111">Der Name einer Zertifikat Vorlage.</span><span class="sxs-lookup"><span data-stu-id="0157b-111">The name of a certificate template.</span></span>
    -   <span data-ttu-id="0157b-112">Der Name des Benutzers, der das Zertifikat anfordert.</span><span class="sxs-lookup"><span data-stu-id="0157b-112">The name of the user requesting the certificate.</span></span>
    -   <span data-ttu-id="0157b-113">Der Name einer PFX-Datei (Personal Information Exchange), in der die Anforderung gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0157b-113">The name of a Personal Information Exchange (PFX) file in which to save the request.</span></span>
    -   <span data-ttu-id="0157b-114">Ein Kennwort, das mit der PFX-Datei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0157b-114">A password to use with the PFX file.</span></span>
    -   <span data-ttu-id="0157b-115">Ein optionaler Name des Registrierungs-Agents.</span><span class="sxs-lookup"><span data-stu-id="0157b-115">An optional enrollment agent template name.</span></span> <span data-ttu-id="0157b-116">Die Vorlage wird verwendet, um ein anmeldungsagentzertifikat zu erstellen, wenn keine im Zertifikat Speicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0157b-116">The template is used to create an enrollment agent certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="0157b-117">Erstellt ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt und initialisiert es mithilfe der Zertifikat Vorlage, die in der Befehlszeile angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0157b-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the certificate template specified on the command line.</span></span>
3.  <span data-ttu-id="0157b-118">Fügt dem Objekt "CMC Request" den Namen des Anforderers hinzu.</span><span class="sxs-lookup"><span data-stu-id="0157b-118">Adds the name of the requester to the CMC request object.</span></span>
4.  <span data-ttu-id="0157b-119">Ruft ein vorhandenes Registrierungs-Agent-Zertifikat ab oder erstellt, sofern nicht gefunden, eine Zertifikat Anforderung von der in der Befehlszeile angegebenen anmeldungsagentvorlage und versucht, es zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="0157b-119">Retrieves an existing enrollment agent certificate or, if one cannot be found, creates a certificate request from the enrollment agent template specified on the command line and attempts to enroll it.</span></span>
5.  <span data-ttu-id="0157b-120">Überprüft die Zertifikat Kette, die das anmeldungsagentzertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="0157b-120">Verifies the certificate chain that contains the enrollment agent certificate.</span></span>
6.  <span data-ttu-id="0157b-121">Erstellt ein [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) -Objekt, initialisiert es mit dem Registrierungs-Agent-Zertifikat, ruft die [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) -Auflistung aus dem Objekt "CMC Request" ab und fügt das Registrierungs-Agent-Signaturzertifikat der Auflistung hinzu.</span><span class="sxs-lookup"><span data-stu-id="0157b-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the enrollment agent certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the enrollment agent signing certificate object to the collection.</span></span> <span data-ttu-id="0157b-122">Das [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, das im nächsten Schritt erläutert wird, verwendet das Zertifikat zum Signieren der CMC-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0157b-122">The [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object discussed in the next step uses the certificate to sign the CMC request.</span></span>
7.  <span data-ttu-id="0157b-123">Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, initialisiert es mithilfe der CMC-Anforderung, versucht, es zu registrieren, und überprüft den Fortschritt des Registrierungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="0157b-123">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, attempts to enroll it, and checks the progress of the enrollment process.</span></span>
8.  <span data-ttu-id="0157b-124">Exportiert das installierte Zertifikat in eine PFX-Datei.</span><span class="sxs-lookup"><span data-stu-id="0157b-124">Exports the installed certificate to a PFX file.</span></span> <span data-ttu-id="0157b-125">Die Datei wird mit dem in der Befehlszeile angegebenen Kennwort geschützt.</span><span class="sxs-lookup"><span data-stu-id="0157b-125">The file is protected by using the password specified on the command line.</span></span> <span data-ttu-id="0157b-126">Die encodedefilew-Funktion ist in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="0157b-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>
9.  <span data-ttu-id="0157b-127">Löscht das Zertifikat aus dem Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="0157b-127">Deletes the certificate from the certificate store.</span></span> <span data-ttu-id="0157b-128">Die im folgenden Codebeispiel verwendeten Funktionen finden Sie in der CryptoAPI-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="0157b-128">The functions used in the following code example can be found in the CryptoAPI documentation.</span></span>
10. <span data-ttu-id="0157b-129">Löscht den privaten Schlüssel vom Computer.</span><span class="sxs-lookup"><span data-stu-id="0157b-129">Deletes the private key from the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0157b-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0157b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0157b-131">CMC eobo-Anforderung</span><span class="sxs-lookup"><span data-stu-id="0157b-131">CMC EOBO Request</span></span>](cmc-eobo-request.md)
</dt> <dt>

[<span data-ttu-id="0157b-132">PKCS \# 10-Anforderung</span><span class="sxs-lookup"><span data-stu-id="0157b-132">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="0157b-133">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="0157b-133">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



