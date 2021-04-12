---
title: Lizenz Sperr-Agent-Objekt
description: Lizenz Sperr-Agent-Objekt
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- Windows Media-Format-SDK, Lizenz Sperr-agentobjekte
- Advanced Systems Format (ASF), Lizenz Sperr-agentobjekte
- ASF (Advanced Systems Format), Lizenz Sperr-agentobjekte
- Objekte, Lizenz Sperr-agentobjekte
- Lizenz Sperrung, Lizenz Sperr-agentobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389844"
---
# <a name="license-revocation-agent-object"></a><span data-ttu-id="3b236-108">Lizenz Sperr-Agent-Objekt</span><span class="sxs-lookup"><span data-stu-id="3b236-108">License Revocation Agent Object</span></span>

<span data-ttu-id="3b236-109">Das Lizenz Sperr-Agent-Objekt verwaltet die Clientseite der Lizenz Sperrung.</span><span class="sxs-lookup"><span data-stu-id="3b236-109">The license revocation agent object manages the client side of license revocation.</span></span> <span data-ttu-id="3b236-110">Der Lizenz Widerruf ist der Prozess, mit dem ein Lizenzserver Lizenzen aus dem Lizenz Speicher auf dem Client Computer entfernen kann.</span><span class="sxs-lookup"><span data-stu-id="3b236-110">License revocation is the process by which a license server can remove licenses from the license store on the client computer.</span></span> <span data-ttu-id="3b236-111">Der Prozess umfasst das übergeben mehrerer Nachrichten zwischen der Client Anwendung und dem Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="3b236-111">The process involves passing several messages between the client application and the license server.</span></span> <span data-ttu-id="3b236-112">Die Methoden, die für dieses Objekt verfügbar gemacht werden, verarbeiten und generieren diese Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="3b236-112">The methods exposed on this object process and generate those messages.</span></span>

<span data-ttu-id="3b236-113">Das Lizenz Sperr-Agent-Objekt wird von der [**wmkreatelicenserevocationagent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) -Funktion erstellt, mit der ein Zeiger auf eine [**iwmlicenserevocationagent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) -Schnittstelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3b236-113">The license revocation agent object is created by the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function, which sets a pointer to an [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span> <span data-ttu-id="3b236-114">**IUnknown** und **iwmlicenserevocationagent** sind die einzigen Schnittstellen, die von diesem Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3b236-114">**IUnknown** and **IWMLicenseRevocationAgent** are the only interfaces supported by this object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b236-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b236-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b236-116">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="3b236-116">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




