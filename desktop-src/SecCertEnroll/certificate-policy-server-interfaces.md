---
description: Die folgenden Schnittstellen können verwendet werden, um einen Zertifikatregistrierungs-Richtlinien Server (Certificate Registrierungs Policy, CEP) Programm gesteuert zu konfigurieren.
ms.assetid: 48c7c21c-1b20-4a79-932d-bed19ff9833e
title: Zertifikat Richtlinien Server-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50c16373c2bac364a91af2cdadf6a8d33445e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527632"
---
# <a name="certificate-policy-server-interfaces"></a><span data-ttu-id="26e93-103">Zertifikat Richtlinien Server-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="26e93-103">Certificate Policy Server Interfaces</span></span>

<span data-ttu-id="26e93-104">Die folgenden Schnittstellen können verwendet werden, um einen Zertifikatregistrierungs-Richtlinien Server (Certificate Registrierungs Policy, CEP) Programm gesteuert zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="26e93-104">The following interfaces can be used to programmatically configure a certificate enrollment policy (CEP) server.</span></span>



| <span data-ttu-id="26e93-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="26e93-105">Interface</span></span>                                                            | <span data-ttu-id="26e93-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26e93-106">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26e93-107">**IX509EnrollmentPolicyServer**</span><span class="sxs-lookup"><span data-stu-id="26e93-107">**IX509EnrollmentPolicyServer**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmentpolicyserver)   | <span data-ttu-id="26e93-108">Stellt einen CEP-Server dar.</span><span class="sxs-lookup"><span data-stu-id="26e93-108">Represents a CEP server.</span></span>                                                                                      |
| [<span data-ttu-id="26e93-109">**IX509PolicyServerListManager**</span><span class="sxs-lookup"><span data-stu-id="26e93-109">**IX509PolicyServerListManager**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509policyserverlistmanager) | <span data-ttu-id="26e93-110">Verwaltet eine Auflistung von [**IX509PolicyServerUrl**](/windows/desktop/api/Certenroll/nn-certenroll-ix509policyserverurl) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="26e93-110">Manages a collection of [**IX509PolicyServerUrl**](/windows/desktop/api/Certenroll/nn-certenroll-ix509policyserverurl) objects.</span></span>                         |
| [<span data-ttu-id="26e93-111">**IX509PolicyServerUrl**</span><span class="sxs-lookup"><span data-stu-id="26e93-111">**IX509PolicyServerUrl**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509policyserverurl)                 | <span data-ttu-id="26e93-112">Gibt die dem CEP-Server zugeordneten Eigenschaftswerte an oder ruft diese ab und aktualisiert zugehörige Registrierungs Werte.</span><span class="sxs-lookup"><span data-stu-id="26e93-112">Specifies or retrieves property values associated with the CEP server and updates associated registry values.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="26e93-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26e93-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26e93-114">CertEnroll-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="26e93-114">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



