---
description: Erstellt eine CMC-Zertifikat Anforderung zum Archivieren eines privaten Schlüssels auf einer Zertifizierungsstelle (Certification Authority, ca).
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: Registrierungsschlüssel archivalcmc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346993"
---
# <a name="enrollkeyarchivalcmc"></a><span data-ttu-id="870c1-103">Registrierungsschlüssel archivalcmc</span><span class="sxs-lookup"><span data-stu-id="870c1-103">enrollKeyArchivalCMC</span></span>

<span data-ttu-id="870c1-104">Das Registrierungs keyarchivalcmc-Beispiel erstellt eine CMC-Zertifikat Anforderung zum Archivieren eines privaten Schlüssels auf einer Zertifizierungsstelle (Certification Authority, ca).</span><span class="sxs-lookup"><span data-stu-id="870c1-104">The enrollKeyArchivalCMC sample creates a CMC certificate request to archive a private key on a certification authority (CA).</span></span> <span data-ttu-id="870c1-105">Weitere Informationen finden Sie unter [CMC-Schlüssel Archivierungs Anforderung](cmc-key-archival-request.md).</span><span class="sxs-lookup"><span data-stu-id="870c1-105">For more information, see [CMC Key Archival Request](cmc-key-archival-request.md).</span></span>

## <a name="location"></a><span data-ttu-id="870c1-106">Standort</span><span class="sxs-lookup"><span data-stu-id="870c1-106">Location</span></span>

<span data-ttu-id="870c1-107">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Einschreibung \\ VC \\ registrierungskeyarchivalcmc installiert.</span><span class="sxs-lookup"><span data-stu-id="870c1-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollKeyArchivalCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="870c1-108">Diskussion</span><span class="sxs-lookup"><span data-stu-id="870c1-108">Discussion</span></span>

<span data-ttu-id="870c1-109">Das Beispiel "registrikeyarchivalcmc":</span><span class="sxs-lookup"><span data-stu-id="870c1-109">The enrollKeyArchivalCMC sample:</span></span>

1.  <span data-ttu-id="870c1-110">Verarbeitet die Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="870c1-110">Processes the command line arguments.</span></span> <span data-ttu-id="870c1-111">Die Befehlszeile muss den Namen der Zertifikat Vorlage enthalten, die für die Anmeldung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="870c1-111">The command line should contain the name of the certificate template to use for enrollment.</span></span>
2.  <span data-ttu-id="870c1-112">Erstellt ein [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) Certificate Request-Objekt und initialisiert es mit dem Vorlagen Namen für einen Endbenutzer Kontext.</span><span class="sxs-lookup"><span data-stu-id="870c1-112">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) certificate request object and initializes it for an end-user context by using the template name.</span></span>
3.  <span data-ttu-id="870c1-113">Legt die [**archiveprivatekey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) -Eigenschaft für die CMC-Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="870c1-113">Sets the [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) property on the CMC request.</span></span>
4.  <span data-ttu-id="870c1-114">Erstellt ein [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) -Objekt und verwendet es, um eine Zeichenfolge abzurufen, die die Zertifizierungsstellen Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="870c1-114">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
5.  <span data-ttu-id="870c1-115">Erstellt ein CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) -Objekt und verwendet es, um das Exchange-Zertifikat für die Zertifizierungsstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="870c1-115">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it to retrieve the exchange certificate for the CA.</span></span>
6.  <span data-ttu-id="870c1-116">Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt, initialisiert es mithilfe der CMC-Anforderung, erstellt eine Base64-codierte Zeichenfolge, die die Schlüssel Archivierungs Anforderung enthält, und sendet Sie an die Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="870c1-116">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, creates a base64 encoded string that contains the key archival request, and submits it to the CA.</span></span>

## <a name="related-topics"></a><span data-ttu-id="870c1-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="870c1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="870c1-118">CMC-Schlüssel Archivierungs Anforderung</span><span class="sxs-lookup"><span data-stu-id="870c1-118">CMC Key Archival Request</span></span>](cmc-key-archival-request.md)
</dt> <dt>

[<span data-ttu-id="870c1-119">CMC-Anforderung</span><span class="sxs-lookup"><span data-stu-id="870c1-119">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="870c1-120">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="870c1-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
