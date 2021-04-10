---
description: Registriert einen Endbenutzer mit einer Zertifizierungsstelle (Certification Authority, ca), indem er eine Vorlage, den Antragsteller Namen und die Länge des Schlüssels in Bits verwendet.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: Registrierungs simpleusercert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042486"
---
# <a name="enrollsimpleusercert"></a><span data-ttu-id="571c1-103">Registrierungs simpleusercert</span><span class="sxs-lookup"><span data-stu-id="571c1-103">enrollSimpleUserCert</span></span>

<span data-ttu-id="571c1-104">Das Beispiel "anmelsimpleusercert" registriert einen Endbenutzer mit einer Zertifizierungsstelle (Certification Authority, ca), indem er eine Vorlage, den Antragsteller Namen und die Länge des Schlüssels in Bits verwendet.</span><span class="sxs-lookup"><span data-stu-id="571c1-104">The enrollSimpleUserCert sample enrolls an end user with a certification authority (CA) by using a template, the subject name, and the length, in bits, of the key.</span></span>

## <a name="location"></a><span data-ttu-id="571c1-105">Standort</span><span class="sxs-lookup"><span data-stu-id="571c1-105">Location</span></span>

<span data-ttu-id="571c1-106">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird eine C++-Version des Beispiels standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Registrierung \\ VC \\ registrisimpleusercert installiert.</span><span class="sxs-lookup"><span data-stu-id="571c1-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollSimpleUserCert folder.</span></span> <span data-ttu-id="571c1-107">Eine c#-Version ist im Ordner *% Program Files%* \\ Microsoft SDRs \\ Windows \\ v 7.0 \\ Samples \\ X509 Certificate Einschreibung \\ csharp \\ registrisimpleusercert installiert.</span><span class="sxs-lookup"><span data-stu-id="571c1-107">A C# version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\CSharp\\EnrollSimpleUserCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="571c1-108">Diskussion</span><span class="sxs-lookup"><span data-stu-id="571c1-108">Discussion</span></span>

<span data-ttu-id="571c1-109">Das Beispiel "registrisimpleusercert":</span><span class="sxs-lookup"><span data-stu-id="571c1-109">The enrollSimpleUserCert sample:</span></span>

1.  <span data-ttu-id="571c1-110">Verarbeitet die Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="571c1-110">Processes the command line arguments.</span></span> <span data-ttu-id="571c1-111">Die Befehlszeile muss den Namen der Vorlage, den Antragsteller Namen und die Schlüssellänge enthalten.</span><span class="sxs-lookup"><span data-stu-id="571c1-111">The command line should contain the name of the template, the subject name, and the key length.</span></span>
2.  <span data-ttu-id="571c1-112">Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt und initialisiert es mithilfe der Vorlage.</span><span class="sxs-lookup"><span data-stu-id="571c1-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template.</span></span>
3.  <span data-ttu-id="571c1-113">Ruft das Objekt der inneren Zertifikat Anforderung aus dem Anmeld-Objekt ab und fragt es nach dem [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="571c1-113">Retrieves the inner certificate request object from the enrollment object and queries it for the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span> <span data-ttu-id="571c1-114">Die innerste Anforderung ist immer eine PKCS \# 10-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="571c1-114">The innermost request is always a PKCS \#10 request.</span></span>
4.  <span data-ttu-id="571c1-115">Ruft das [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) -Objekt aus der PKCS \# 10-Anforderung ab und legt die in der Befehlszeile angegebene Schlüssellänge fest.</span><span class="sxs-lookup"><span data-stu-id="571c1-115">Retrieves the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object from the PKCS \#10 request and sets the key length specified on the command line.</span></span>
5.  <span data-ttu-id="571c1-116">Erstellt ein [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) -Objekt, verwendet es, um den X. 500-Betreffnamen zu codieren, und fügt den Namen der PKCS \# 10-Anforderung hinzu.</span><span class="sxs-lookup"><span data-stu-id="571c1-116">Creates an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, uses it to encode the X.500 subject name, and adds the name to the PKCS \#10 request.</span></span>
6.  <span data-ttu-id="571c1-117">Versucht, den Endbenutzer bei der Zertifizierungsstelle zu registrieren und den Fortschritt des Registrierungsvorgangs zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="571c1-117">Attempts to enroll the end user with the CA and monitors the progress of the enrollment process.</span></span> <span data-ttu-id="571c1-118">Die Funktion "checkenrollstatus" wird in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="571c1-118">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="571c1-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="571c1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="571c1-120">PKCS \# 10-Anforderung</span><span class="sxs-lookup"><span data-stu-id="571c1-120">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="571c1-121">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="571c1-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



