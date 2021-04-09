---
description: Die Xenroll.dll Bibliothek wurde aus dem Betriebssystem entfernt und durch CertEnroll.dll ersetzt.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Zuordnung von Xenroll.dll zu CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758059"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a><span data-ttu-id="e40b6-103">Zuordnung von Xenroll.dll zu CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="e40b6-103">Mapping Xenroll.dll to CertEnroll.dll</span></span>

<span data-ttu-id="e40b6-104">Vor Windows Vista wurde die Zertifikat Registrierungs Steuerung in Xenroll.dll implementiert.</span><span class="sxs-lookup"><span data-stu-id="e40b6-104">Prior to Windows Vista, the Certificate Enrollment Control was implemented in Xenroll.dll.</span></span> <span data-ttu-id="e40b6-105">Die Xenroll.dll Bibliothek wurde aus dem Betriebssystem entfernt und durch CertEnroll.dll ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e40b6-105">The Xenroll.dll library has been removed from the operating system and replaced by CertEnroll.dll.</span></span>

<span data-ttu-id="e40b6-106">XEnroll versuchte, zwei parallele Sätze von Schnittstellen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="e40b6-106">Xenroll attempted to implement two parallel sets of interfaces.</span></span> <span data-ttu-id="e40b6-107">[**Icenroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)und [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) waren Automatisierungs konform und kompatibel mit Skriptsprachen.</span><span class="sxs-lookup"><span data-stu-id="e40b6-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3), and [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) were Automation-compliant and compatible with scripting languages.</span></span> <span data-ttu-id="e40b6-108">Die entsprechenden Schnittstellen –[**ienroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)und [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)– konnten nicht in die Skripterstellung einbezogen werden, wurden jedoch für C++ Programmierer besser geeignet.</span><span class="sxs-lookup"><span data-stu-id="e40b6-108">The corresponding interfaces—[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2), and [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)—could not be scripted but were more convenient for C++ programmers.</span></span> <span data-ttu-id="e40b6-109">Wenn Sie sich entwickelt haben, wurden die beiden Schnittstellen Sätze nicht synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="e40b6-109">As they evolved, the two sets of interfaces did not remain synchronized.</span></span> <span data-ttu-id="e40b6-110">Insbesondere definiert der Satz von Dual Schnittstellen, der von **ICEnroll4** zuletzt dargestellt wird, nur eine Teilmenge der von **IEnroll4** definierten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e40b6-110">In particular, the set of dual interfaces represented most recently by **ICEnroll4** defines only a subset of the functionality defined by **IEnroll4**.</span></span>

<span data-ttu-id="e40b6-111">CertEnroll.dll implementiert einen größeren und strukturierteren Satz von Automatisierungs kompatiblen com-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="e40b6-111">CertEnroll.dll implements a larger and more structured set of Automation-compliant COM interfaces.</span></span> <span data-ttu-id="e40b6-112">In den folgenden Themen wird erläutert, wie Xenroll.dll CertEnroll.dll für verschiedene Funktionstypen zuordnet.</span><span class="sxs-lookup"><span data-stu-id="e40b6-112">The following topics discuss how Xenroll.dll maps to CertEnroll.dll for different types of functionality.</span></span>

-   [<span data-ttu-id="e40b6-113">Zertifikat Anforderungs Funktionen</span><span class="sxs-lookup"><span data-stu-id="e40b6-113">Certificate Request Functions</span></span>](certificate-request-functions.md)
-   [<span data-ttu-id="e40b6-114">Funktionen für Zertifikat Antworten</span><span class="sxs-lookup"><span data-stu-id="e40b6-114">Certificate Response Functions</span></span>](certificate-response-functions.md)
-   [<span data-ttu-id="e40b6-115">Attribut Funktionen</span><span class="sxs-lookup"><span data-stu-id="e40b6-115">Attribute Functions</span></span>](attribute-functions.md)
-   [<span data-ttu-id="e40b6-116">Erweiterungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="e40b6-116">Extension Functions</span></span>](extension-functions.md)
-   [<span data-ttu-id="e40b6-117">Externe Eigenschaften Funktionen</span><span class="sxs-lookup"><span data-stu-id="e40b6-117">External Property Functions</span></span>](external-property-functions.md)
-   [<span data-ttu-id="e40b6-118">Funktionen für private und öffentliche Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e40b6-118">Private and Public Key Functions</span></span>](private-and-public-key-functions.md)
-   [<span data-ttu-id="e40b6-119">Kryptografiedienstanbieter-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e40b6-119">Cryptographic Service Provider Functions</span></span>](cryptographic-service-provider-functions.md)
-   [<span data-ttu-id="e40b6-120">Zertifikat Speicherfunktionen</span><span class="sxs-lookup"><span data-stu-id="e40b6-120">Certificate Store Functions</span></span>](certificate-store-functions.md)
-   [<span data-ttu-id="e40b6-121">Funktionen für den persönlichen Informationsaustausch</span><span class="sxs-lookup"><span data-stu-id="e40b6-121">Personal Information Exchange Functions</span></span>](personal-information-exchange-functions.md)
-   [<span data-ttu-id="e40b6-122">Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="e40b6-122">Helper Functions</span></span>](helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="e40b6-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e40b6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e40b6-124">Verwenden der Zertifikatregistrierungs-API</span><span class="sxs-lookup"><span data-stu-id="e40b6-124">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
