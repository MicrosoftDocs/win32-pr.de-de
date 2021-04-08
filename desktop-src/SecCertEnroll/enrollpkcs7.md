---
description: Erstellt eine PKCS \# 7-Anforderung von einem vorhandenen Zertifikat, indem die öffentlichen und privaten Schlüssel und die Zertifikat Vorlage geerbt werden.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34bc7f9d7b7d5ae9fa88db0dd70c177c3aa69da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750017"
---
# <a name="enrollpkcs7"></a><span data-ttu-id="a70fb-103">enrollPKCS7</span><span class="sxs-lookup"><span data-stu-id="a70fb-103">enrollPKCS7</span></span>

<span data-ttu-id="a70fb-104">Das enrollPKCS7-Beispiel erstellt eine PKCS \# 7-Anforderung von einem vorhandenen Zertifikat, indem die öffentlichen und privaten Schlüssel und die Zertifikat Vorlage geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="a70fb-104">The enrollPKCS7 sample creates a PKCS \#7 request from an existing certificate by inheriting the public and private keys and the certificate template.</span></span> <span data-ttu-id="a70fb-105">Das vorhandene Zertifikat wird verwendet, um die Anforderung zu signieren.</span><span class="sxs-lookup"><span data-stu-id="a70fb-105">The existing certificate is used to sign the request.</span></span> <span data-ttu-id="a70fb-106">In diesem Beispiel wird der Benutzer in einer Zertifikat Hierarchie registriert und die Zertifikats Antwort installiert.</span><span class="sxs-lookup"><span data-stu-id="a70fb-106">This sample enrolls the user in a certificate hierarchy and installs the certificate response.</span></span> <span data-ttu-id="a70fb-107">Im Beispiel wird ein vorhandenes Zertifikat verwendet, um ein neues Zertifikat zu registrieren und zu installieren.</span><span class="sxs-lookup"><span data-stu-id="a70fb-107">The sample uses an existing certificate to enroll and install a new one.</span></span> <span data-ttu-id="a70fb-108">Weitere Informationen zum Erneuern eines vorhandenen Zertifikats finden Sie unter [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span><span class="sxs-lookup"><span data-stu-id="a70fb-108">For more information about renewing an existing certificate, see [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span></span>

## <a name="location"></a><span data-ttu-id="a70fb-109">Standort</span><span class="sxs-lookup"><span data-stu-id="a70fb-109">Location</span></span>

<span data-ttu-id="a70fb-110">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Einschreibung \\ VC \\ enrollPKCS7 installiert.</span><span class="sxs-lookup"><span data-stu-id="a70fb-110">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="a70fb-111">Diskussion</span><span class="sxs-lookup"><span data-stu-id="a70fb-111">Discussion</span></span>

<span data-ttu-id="a70fb-112">Das enrollPKCS7-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a70fb-112">The enrollPKCS7 sample:</span></span>

1.  <span data-ttu-id="a70fb-113">Verarbeitet die Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="a70fb-113">Processes the command line arguments.</span></span> <span data-ttu-id="a70fb-114">Die Befehlszeile muss den Namen der Zertifikat Vorlage enthalten, die für die Suche nach einem vorhandenen Zertifikat verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a70fb-114">The command line should contain the name of the certificate template used to find an existing certificate.</span></span>
2.  <span data-ttu-id="a70fb-115">Ruft ein vorhandenes Zertifikat mit dem Namen der Vorlage ab, die in der Befehlszeile angegeben ist, oder wenn ein Zertifikat nicht gefunden werden kann, versucht, eine neue zu registrieren, die mithilfe der Vorlage erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a70fb-115">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll a new one created by using the template.</span></span> <span data-ttu-id="a70fb-116">Die Funktionen "findcertbytemplate" und "registricertbytemplate" sind in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="a70fb-116">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="a70fb-117">Überprüft die Zertifikat Kette und konvertiert das Zertifikat in ein **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="a70fb-117">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="a70fb-118">Erstellt ein [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) -Objekt und initialisiert es mithilfe des vorhandenen Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="a70fb-118">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="a70fb-119">Das neue PKCS \# 7-Anforderungs Objekt erbt die privaten und öffentlichen Schlüssel und die Vorlage aus dem vorhandenen Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="a70fb-119">The new PKCS \#7 request object inherits the private and public keys and template from the existing certificate.</span></span>
5.  <span data-ttu-id="a70fb-120">Erstellt ein [**isignercertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) -Objekt, initialisiert es mit dem vorhandenen Zertifikat und fügt es dem PKCS 7- \# Anforderungs Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="a70fb-120">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the existing certificate, and adds it to the PKCS \#7 request object.</span></span>
6.  <span data-ttu-id="a70fb-121">Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, initialisiert es mit dem PKCS \# 7-Anforderungs Objekt, versucht, es bei der Zertifizierungsstelle zu registrieren, und überwacht den Status des Registrierungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="a70fb-121">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="a70fb-122">Die Funktion "checkenrollstatus" wird in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="a70fb-122">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a70fb-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a70fb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a70fb-124">CMC-Anforderung</span><span class="sxs-lookup"><span data-stu-id="a70fb-124">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="a70fb-125">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="a70fb-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



