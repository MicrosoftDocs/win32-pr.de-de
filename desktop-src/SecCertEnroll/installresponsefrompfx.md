---
description: Installiert ein registriertes Zertifikat aus einer PFX-Datei (Personal Information Exchange) im Zertifikat Speicher.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: InstallResponse-frompfx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960463"
---
# <a name="installresponsefrompfx"></a><span data-ttu-id="49476-103">InstallResponse-frompfx</span><span class="sxs-lookup"><span data-stu-id="49476-103">installResponseFromPFX</span></span>

<span data-ttu-id="49476-104">Mit dem Beispiel "installresponstifrompfx" wird ein registriertes Zertifikat aus einer PFX-Datei (Personal Information Exchange) in den Zertifikat Speicher installiert.</span><span class="sxs-lookup"><span data-stu-id="49476-104">The installResponseFromPFX sample installs an enrolled certificate from a Personal Information Exchange (PFX) file to the certificate store.</span></span>

## <a name="location"></a><span data-ttu-id="49476-105">Standort</span><span class="sxs-lookup"><span data-stu-id="49476-105">Location</span></span>

<span data-ttu-id="49476-106">Wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren, wird das Beispiel standardmäßig im Ordner *% Program Files%* \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate Einschreibung \\ VC \\ installresponsefrompfx installiert.</span><span class="sxs-lookup"><span data-stu-id="49476-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\installResponseFromPFX folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="49476-107">Diskussion</span><span class="sxs-lookup"><span data-stu-id="49476-107">Discussion</span></span>

<span data-ttu-id="49476-108">Das InstallResponse-frompfx-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="49476-108">The installResponseFromPFX sample:</span></span>

1.  <span data-ttu-id="49476-109">Verarbeitet die Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="49476-109">Processes the command line arguments.</span></span> <span data-ttu-id="49476-110">Die Befehlszeile sollte Folgendes enthalten:</span><span class="sxs-lookup"><span data-stu-id="49476-110">The command line should contain:</span></span>
    -   <span data-ttu-id="49476-111">Der Name des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="49476-111">The name of the sample.</span></span>
    -   <span data-ttu-id="49476-112">Der Name der PFX-Datei, die das registrierte Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="49476-112">The name of the PFX file that contains the enrolled certificate.</span></span>
    -   <span data-ttu-id="49476-113">Ein Kennwort, das der PFX-Datei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="49476-113">A password associated with the PFX file.</span></span>
2.  <span data-ttu-id="49476-114">Liest die PFX-Datei, versucht zunächst das Base64-Format und das Binärformat, wenn Base64 fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="49476-114">Reads the PFX file, trying the base64 format first and the binary format if base64 fails.</span></span> <span data-ttu-id="49476-115">Die decodefilew ()-Funktion wird in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="49476-115">The DecodeFileW() function is defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="49476-116">Konvertiert das registrierte Zertifikat in ein **BSTR** und verwendet es, um ein [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="49476-116">Converts the enrolled certificate to a **BSTR** and uses it to initialize an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object.</span></span> <span data-ttu-id="49476-117">Die convertwszdebstr-Funktion ist in der Datei "registricommon. cpp" definiert.</span><span class="sxs-lookup"><span data-stu-id="49476-117">The convertWszToBstr function is defined in enrollCommon.cpp.</span></span>
4.  <span data-ttu-id="49476-118">Installiert das Zertifikat im Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="49476-118">Installs the certificate in the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49476-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49476-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49476-120">Einschreibung von "Einschreibung"</span><span class="sxs-lookup"><span data-stu-id="49476-120">enrollEOBOCMC</span></span>](enrolleobocmc.md)
</dt> <dt>

[<span data-ttu-id="49476-121">Verwenden der enthaltenen Beispiele</span><span class="sxs-lookup"><span data-stu-id="49476-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



