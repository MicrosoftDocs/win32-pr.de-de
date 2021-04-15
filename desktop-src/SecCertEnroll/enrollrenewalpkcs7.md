---
description: Erstellt ein PKCS \# 7-Anforderungs Objekt, um ein vorhandenes Zertifikat zu erneuern. Das Anforderungs Objekt verwendet ein neues Schlüsselpaar, behält jedoch den Kryptografieanbieter bei, der dem erneuert-Zertifikat zugeordnet ist.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8795758a2744dcee07a100f87eb1db0a1af49eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529390"
---
# <a name="enrollrenewalpkcs7"></a><span data-ttu-id="35b08-104">enrollRenewalPKCS7</span><span class="sxs-lookup"><span data-stu-id="35b08-104">enrollRenewalPKCS7</span></span>

<span data-ttu-id="35b08-105">Das enrollRenewalPKCS7-Beispiel erstellt ein PKCS \# 7-Anforderungs Objekt, um ein vorhandenes Zertifikat zu erneuern.</span><span class="sxs-lookup"><span data-stu-id="35b08-105">The enrollRenewalPKCS7 sample creates a PKCS \#7 request object to renew an existing certificate.</span></span> <span data-ttu-id="35b08-106">Das Anforderungs Objekt verwendet ein neues Schlüsselpaar, behält jedoch den Kryptografieanbieter bei, der dem erneuert-Zertifikat zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="35b08-106">The request object uses a new key pair but retains the cryptographic provider associated with the certificate being renewed.</span></span>

## <a name="location"></a><span data-ttu-id="35b08-107">Standort</span><span class="sxs-lookup"><span data-stu-id="35b08-107">Location</span></span>

<span data-ttu-id="35b08-108">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Einschreibung \\ VC \\ enrollRenewalPKCS7 installiert.</span><span class="sxs-lookup"><span data-stu-id="35b08-108">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollRenewalPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="35b08-109">Diskussion</span><span class="sxs-lookup"><span data-stu-id="35b08-109">Discussion</span></span>

<span data-ttu-id="35b08-110">Das enrollRenewalPKCS7-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="35b08-110">The enrollRenewalPKCS7 sample:</span></span>

1.  <span data-ttu-id="35b08-111">Verarbeitet die Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="35b08-111">Processes the command line arguments.</span></span> <span data-ttu-id="35b08-112">Die Befehlszeile muss den Namen der Vorlage enthalten, die zum Erstellen der Zertifikat Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="35b08-112">The command line should contain the name of the template used to create the certificate request.</span></span>
2.  <span data-ttu-id="35b08-113">Ruft ein vorhandenes Zertifikat mit dem Namen der Vorlage ab, die in der Befehlszeile angegeben ist, oder wenn ein Zertifikat nicht gefunden werden kann, versucht, ein Zertifikat mithilfe der Vorlage zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="35b08-113">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll one by using the template.</span></span> <span data-ttu-id="35b08-114">Die Funktionen "findcertbytemplate" und "registricertbytemplate" sind in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="35b08-114">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="35b08-115">Überprüft die Zertifikat Kette und konvertiert das Zertifikat in ein **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="35b08-115">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="35b08-116">Erstellt ein [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) -Objekt und initialisiert es mithilfe des vorhandenen Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="35b08-116">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="35b08-117">Da der Parameter " *geerbt Options* " auf "geerbt default" festgelegt ist, wird ein neues Schlüsselpaar für die Anforderung erstellt, aber der Kryptografieanbieter im vorhandenen Zertifikat wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="35b08-117">Because the *inheritOptions* parameter is set to InheritDefault, a new key pair is created for the request but the cryptographic provider in the existing certificate is used.</span></span> <span data-ttu-id="35b08-118">Weitere Informationen finden Sie unter der [**initializefromcertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) -Methode.</span><span class="sxs-lookup"><span data-stu-id="35b08-118">For more information, see the [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) method.</span></span>
5.  <span data-ttu-id="35b08-119">Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, initialisiert es mit dem PKCS \# 7-Anforderungs Objekt, versucht, es bei der Zertifizierungsstelle zu registrieren, und überwacht den Status des Registrierungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="35b08-119">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="35b08-120">Die Funktion "checkenrollstatus" wird in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="35b08-120">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35b08-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35b08-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35b08-122">CMC-Anforderung</span><span class="sxs-lookup"><span data-stu-id="35b08-122">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="35b08-123">PKCS \# 7-Erneuerungs Anforderung</span><span class="sxs-lookup"><span data-stu-id="35b08-123">PKCS \#7 Renewal Request</span></span>](pkcs--7--renewal-request.md)
</dt> <dt>

[<span data-ttu-id="35b08-124">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="35b08-124">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



