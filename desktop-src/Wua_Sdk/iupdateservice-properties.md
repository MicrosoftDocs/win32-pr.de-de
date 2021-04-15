---
description: Die iupdateservice-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: Iupdateservice-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff3cf92c89a5ba02b7d95f1a1c99f33de3202d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485131"
---
# <a name="iupdateservice-properties"></a><span data-ttu-id="aac4a-103">Iupdateservice-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aac4a-103">IUpdateService Properties</span></span>

<span data-ttu-id="aac4a-104">Die [**iupdateservice**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aac4a-104">The [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface defines the following properties.</span></span>



| <span data-ttu-id="aac4a-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="aac4a-105">Property</span></span>                                                              | <span data-ttu-id="aac4a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aac4a-106">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aac4a-107">**Canregisterwithau**</span><span class="sxs-lookup"><span data-stu-id="aac4a-107">**CanRegisterWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | <span data-ttu-id="aac4a-108">Ruft einen booleschen Wert ab, der angibt, ob der Dienst bei automatische Updates registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="aac4a-108">Gets a Boolean value that indicates whether the service can register with Automatic Updates.</span></span>    |
| [<span data-ttu-id="aac4a-109">**Contentvalidationcert**</span><span class="sxs-lookup"><span data-stu-id="aac4a-109">**ContentValidationCert**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | <span data-ttu-id="aac4a-110">Ruft einen SHA-1-Hash des Zertifikats ab, das verwendet wird, um den Inhalt des Dienstanbieter zu signieren.</span><span class="sxs-lookup"><span data-stu-id="aac4a-110">Gets an SHA-1 hash of the certificate that is used to sign the contents of the service.</span></span>         |
| [<span data-ttu-id="aac4a-111">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="aac4a-111">**ExpirationDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | <span data-ttu-id="aac4a-112">Ruft das Datum ab, an dem die Autorisierungs CAB-Datei abläuft.</span><span class="sxs-lookup"><span data-stu-id="aac4a-112">Gets the date on which the authorization cabinet file expires.</span></span>                                  |
| [<span data-ttu-id="aac4a-113">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="aac4a-113">**IsManaged**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | <span data-ttu-id="aac4a-114">Ruft einen booleschen Wert ab, der angibt, ob ein Dienst ein verwalteter Dienst ist.</span><span class="sxs-lookup"><span data-stu-id="aac4a-114">Gets a Boolean value that indicates whether a service is a managed service.</span></span>                     |
| [<span data-ttu-id="aac4a-115">**Isregisteredwithau**</span><span class="sxs-lookup"><span data-stu-id="aac4a-115">**IsRegisteredWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | <span data-ttu-id="aac4a-116">Ruft einen booleschen Wert ab, der angibt, ob ein Dienst bei automatische Updates registriert ist.</span><span class="sxs-lookup"><span data-stu-id="aac4a-116">Gets a Boolean value that indicates whether a service is registered with Automatic Updates.</span></span>     |
| [<span data-ttu-id="aac4a-117">**Isscanpackageservice**</span><span class="sxs-lookup"><span data-stu-id="aac4a-117">**IsScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | <span data-ttu-id="aac4a-118">Ruft einen booleschen Wert ab, der angibt, ob ein Dienst auf einem Überprüfungspaket basiert.</span><span class="sxs-lookup"><span data-stu-id="aac4a-118">Gets a Boolean value that indicates whether a service is based on a scan package.</span></span>               |
| [<span data-ttu-id="aac4a-119">**IssueDate**</span><span class="sxs-lookup"><span data-stu-id="aac4a-119">**IssueDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | <span data-ttu-id="aac4a-120">Ruft das Datum ab, an dem die Autorisierungs CAB-Datei ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="aac4a-120">Gets the date on which the authorization cabinet file was issued.</span></span>                               |
| [<span data-ttu-id="aac4a-121">**Name**</span><span class="sxs-lookup"><span data-stu-id="aac4a-121">**Name**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | <span data-ttu-id="aac4a-122">Ruft den Namen des Diensts ab.</span><span class="sxs-lookup"><span data-stu-id="aac4a-122">Gets the name of the service.</span></span>                                                                   |
| [<span data-ttu-id="aac4a-123">**Offerswindowsupdates**</span><span class="sxs-lookup"><span data-stu-id="aac4a-123">**OffersWindowsUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | <span data-ttu-id="aac4a-124">Ruft einen booleschen Wert ab, der angibt, ob der aktuelle Dienst Updates von Windows-Updates anbietet.</span><span class="sxs-lookup"><span data-stu-id="aac4a-124">Gets a Boolean value indicates whether the current service offers updates from Windows Updates.</span></span> |
| [<span data-ttu-id="aac4a-125">**Redirecturls**</span><span class="sxs-lookup"><span data-stu-id="aac4a-125">**RedirectUrls**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | <span data-ttu-id="aac4a-126">Ruft die URL für die Redirector-CAB-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="aac4a-126">Gets the URL for the redirector cabinet file.</span></span>                                                   |
| [<span data-ttu-id="aac4a-127">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="aac4a-127">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | <span data-ttu-id="aac4a-128">Ruft den Bezeichner für einen Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="aac4a-128">Gets the identifier for a service.</span></span>                                                              |
| [<span data-ttu-id="aac4a-129">**ServiceUrl**</span><span class="sxs-lookup"><span data-stu-id="aac4a-129">**ServiceUrl**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | <span data-ttu-id="aac4a-130">Ruft die URL für den Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="aac4a-130">Gets the URL for the service.</span></span>                                                                   |
| [<span data-ttu-id="aac4a-131">**Setupprefix**</span><span class="sxs-lookup"><span data-stu-id="aac4a-131">**SetupPrefix**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | <span data-ttu-id="aac4a-132">Ruft das Präfix für die Setup Dateien ab.</span><span class="sxs-lookup"><span data-stu-id="aac4a-132">Gets the prefix for the setup files.</span></span>                                                            |



 

 

 



