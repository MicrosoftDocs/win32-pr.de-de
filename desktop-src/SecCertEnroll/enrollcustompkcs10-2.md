---
description: Erstellt eine benutzerdefinierte PKCS \# 10-Anforderung und versucht, Sie in einer Unternehmens Zertifizierungsstelle (Certification Authority, ca) zu registrieren.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d20615826bb72b6282144b72a394cde41e35910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357390"
---
# <a name="enrollcustompkcs10_2"></a><span data-ttu-id="a3aa5-103">enrollCustomPKCS10 \_ 2</span><span class="sxs-lookup"><span data-stu-id="a3aa5-103">enrollCustomPKCS10\_2</span></span>

<span data-ttu-id="a3aa5-104">Das \_ Beispiel enrollCustomPKCS10 2 erstellt eine benutzerdefinierte PKCS \# 10-Anforderung und versucht, Sie in einer Unternehmens [*Zertifizierungsstelle (Certification Authority*](/windows/desktop/SecGloss/c-gly) , ca) zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="a3aa5-104">The enrollCustomPKCS10\_2 sample creates a custom PKCS \#10 request and attempts to enroll it in an enterprise [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span>

## <a name="location"></a><span data-ttu-id="a3aa5-105">Standort</span><span class="sxs-lookup"><span data-stu-id="a3aa5-105">Location</span></span>

<span data-ttu-id="a3aa5-106">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Einschreibung \\ VC \\ enrollCustomPKCS10 2 installiert \_ .</span><span class="sxs-lookup"><span data-stu-id="a3aa5-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed by default in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomPKCS10\_2 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="a3aa5-107">Diskussion</span><span class="sxs-lookup"><span data-stu-id="a3aa5-107">Discussion</span></span>

<span data-ttu-id="a3aa5-108">Das \_ Beispiel enrollCustomPKCS10 2:</span><span class="sxs-lookup"><span data-stu-id="a3aa5-108">The enrollCustomPKCS10\_2 sample:</span></span>

1.  <span data-ttu-id="a3aa5-109">Verarbeitet die Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="a3aa5-109">Processes the command line arguments.</span></span> <span data-ttu-id="a3aa5-110">Die Befehlszeile sollte den Namen einer Vorlage und den Namen eines Kryptografieanbieters enthalten.</span><span class="sxs-lookup"><span data-stu-id="a3aa5-110">The command line should contain the name of a template and the name of a cryptographic provider.</span></span>
2.  <span data-ttu-id="a3aa5-111">Erstellt ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt und initialisiert es mit dem Namen der Vorlage, die in der Befehlszeile angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a3aa5-111">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the name of the template specified on the command line.</span></span>
3.  <span data-ttu-id="a3aa5-112">Ruft die [*Zertifikat Anforderung*](/windows/desktop/SecGloss/c-gly) aus dem Anmeld ungs Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="a3aa5-112">Retrieves the [*certificate request*](/windows/desktop/SecGloss/c-gly) from the enrollment object.</span></span>
4.  <span data-ttu-id="a3aa5-113">Ruft die innerste PKCS \# 10-Anforderung aus dem Zertifikat Anforderungs Objekt ab, das in Schritt 3 abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="a3aa5-113">Retrieves the innermost PKCS\#10 request from the certificate request object obtained in step 3.</span></span>
5.  <span data-ttu-id="a3aa5-114">Ruft einen [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) aus der PKCS \# 10-Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="a3aa5-114">Retrieves a [*private key*](/windows/desktop/SecGloss/p-gly) from the PKCS\#10 request.</span></span>
6.  <span data-ttu-id="a3aa5-115">Erstellt eine [**icspinformation**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) -Auflistung und fügt der Auflistung die verfügbaren Kryptografieanbieter hinzu und ruft dann ein [**icspstatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) -Objekt für den Anbieter ab, der in der Befehlszeile angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a3aa5-115">Creates an [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) collection and adds the available cryptographic providers to the collection and then retrieves an [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) object for the provider specified on the command line.</span></span>
7.  <span data-ttu-id="a3aa5-116">Legt das Status Objekt für den privaten Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="a3aa5-116">Sets the status object on the private key.</span></span>
8.  <span data-ttu-id="a3aa5-117">Versucht, die [*Zertifikat Anforderung*](/windows/desktop/SecGloss/c-gly)zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="a3aa5-117">Attempts to enroll the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3aa5-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a3aa5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3aa5-119">PKCS \# 10-Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3aa5-119">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="a3aa5-120">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3aa5-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
