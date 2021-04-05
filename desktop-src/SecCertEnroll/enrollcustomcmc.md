---
description: Erstellt eine CMC-Zertifikat Anforderung und registriert einen Computer in einer Zertifikatshierarchie.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: Registrier customcmc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752736"
---
# <a name="enrollcustomcmc"></a><span data-ttu-id="703fc-103">Registrier customcmc</span><span class="sxs-lookup"><span data-stu-id="703fc-103">enrollCustomCMC</span></span>

<span data-ttu-id="703fc-104">Das Beispiel "registricustomcmc" erstellt eine CMC-Zertifikat Anforderung und registriert einen Computer in einer Zertifikatshierarchie.</span><span class="sxs-lookup"><span data-stu-id="703fc-104">The enrollCustomCMC sample creates a CMC certificate request and enrolls a computer in a certificate hierarchy.</span></span>

## <a name="location"></a><span data-ttu-id="703fc-105">Standort</span><span class="sxs-lookup"><span data-stu-id="703fc-105">Location</span></span>

<span data-ttu-id="703fc-106">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC \\ registrierungscustomcmc installiert.</span><span class="sxs-lookup"><span data-stu-id="703fc-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="703fc-107">Diskussion</span><span class="sxs-lookup"><span data-stu-id="703fc-107">Discussion</span></span>

<span data-ttu-id="703fc-108">Das Beispiel "registricustomcmc":</span><span class="sxs-lookup"><span data-stu-id="703fc-108">The enrollCustomCMC sample:</span></span>

1.  <span data-ttu-id="703fc-109">Verarbeitet die folgenden Befehlszeilenargumente:</span><span class="sxs-lookup"><span data-stu-id="703fc-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="703fc-110">Ein benutzerdefiniertes Name-Wert-Paar, das der Zertifikat Anforderung hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="703fc-110">A custom name/value pair to add to the certificate request.</span></span>
    -   <span data-ttu-id="703fc-111">Ein alternativer Antragsteller Name.</span><span class="sxs-lookup"><span data-stu-id="703fc-111">An alternative subject name.</span></span>
    -   <span data-ttu-id="703fc-112">Ein Objekt Bezeichner (OID) für die Erweiterung der erweiterten Schlüssel Verwendung (EKU).</span><span class="sxs-lookup"><span data-stu-id="703fc-112">An object identifier (OID) for the Enhanced Key Usage (EKU) extension.</span></span>
2.  <span data-ttu-id="703fc-113">Erstellt ein [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) Request-Objekt und initialisiert es mithilfe des Computer Kontexts.</span><span class="sxs-lookup"><span data-stu-id="703fc-113">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) request object and initializes it by using the computer context.</span></span>
3.  <span data-ttu-id="703fc-114">Verwendet die PKCS \# 10-Anforderung, um ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) -Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="703fc-114">Uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
4.  <span data-ttu-id="703fc-115">Erstellt ein [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) -Objekt, indem die in der Befehlszeile angegebene OID verwendet und der Erweiterungs Auflistung für die CMC-Anforderung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="703fc-115">Creates an [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) object by using the OID specified on the command line and adds it to the extensions collection for the CMC request.</span></span>
5.  <span data-ttu-id="703fc-116">Erstellt das [**ialternativename**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) -Objekt unter Verwendung des in der Befehlszeile angegebenen Namens, fügt es der [**ialternativenames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) -Auflistung hinzu, verwendet die Auflistung, um eine [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) -Erweiterung zu initialisieren, und fügt diese der Erweiterungs Auflistung für die CMC-Anforderung hinzu.</span><span class="sxs-lookup"><span data-stu-id="703fc-116">Creates [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) object by using the name specified on the command line, adds it to the [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) collection, uses the collection to initialize an [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) extension and adds this to the extensions collection for the CMC request.</span></span>
6.  <span data-ttu-id="703fc-117">Erstellt ein [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) -Objekt mit dem in der Befehlszeile angegebenen Namen und Wert und fügt es der [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) -Auflistung in der CMC-Anforderung hinzu.</span><span class="sxs-lookup"><span data-stu-id="703fc-117">Creates an [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) object by using the name and value specified on the command line, and adds it to the [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection on the CMC request.</span></span>
7.  <span data-ttu-id="703fc-118">Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, initialisiert es mit dem Objekt "CMC Request" und ruft eine Zeichenfolge ab, die eine Base64-codierte Anforderung enthält.</span><span class="sxs-lookup"><span data-stu-id="703fc-118">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request object, and retrieves a string that contains a base64-encoded request.</span></span>
8.  <span data-ttu-id="703fc-119">Erstellt ein [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) -Objekt und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellen Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="703fc-119">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
9.  <span data-ttu-id="703fc-120">Erstellt ein CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) -Objekt und verwendet es sowie die Zeichen folgen, die die Zertifizierungsstellen Konfiguration enthalten, und die Zertifikat Anforderung zum übermitteln der Anforderung an die Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="703fc-120">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
10. <span data-ttu-id="703fc-121">Überprüft den Übermittlungs Status und installiert, wenn erfolgreich, das Zertifikat im Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="703fc-121">Checks the submission status and, if successful, installs the certificate to the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="703fc-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="703fc-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="703fc-123">CMC-Anforderung</span><span class="sxs-lookup"><span data-stu-id="703fc-123">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="703fc-124">PKCS \# 10-Anforderung</span><span class="sxs-lookup"><span data-stu-id="703fc-124">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="703fc-125">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="703fc-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
