---
description: Die folgenden Funktionen werden mit Windows-Security Center verwendet.
ms.assetid: FC28ACD2-A3C6-42A9-AE59-61892A139FB7
title: Windows Security Center-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250d5b3dd7213d9d7f9363ce6b1a83a1e170e01a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860598"
---
# <a name="windows-security-center-functions"></a><span data-ttu-id="1e7f8-103">Windows Security Center-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1e7f8-103">Windows Security Center Functions</span></span>

<span data-ttu-id="1e7f8-104">Die folgenden Funktionen werden mit Windows-Security Center verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e7f8-104">The following functions are used with Windows Security Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1e7f8-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1e7f8-105">In this section</span></span>



| <span data-ttu-id="1e7f8-106">Thema</span><span class="sxs-lookup"><span data-stu-id="1e7f8-106">Topic</span></span>                                                                           | <span data-ttu-id="1e7f8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e7f8-107">Description</span></span>                                                                                                                                                                              |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e7f8-108">**Wscgetsecurityproviderhealth**</span><span class="sxs-lookup"><span data-stu-id="1e7f8-108">**WscGetSecurityProviderHealth**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscgetsecurityproviderhealth)<br/> | <span data-ttu-id="1e7f8-109">Ruft den aggregierten Integritäts Status der Sicherheitsanbieter Kategorien ab, die durch die angegebenen Enumerationswerte des [**WSC- \_ Sicherheits \_ Anbieters**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1e7f8-109">Gets the aggregate health state of the security provider categories represented by the specified [**WSC\_SECURITY\_PROVIDER**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) enumeration values.</span></span><br/> |
| [<span data-ttu-id="1e7f8-110">**Wscregisterforchanges**</span><span class="sxs-lookup"><span data-stu-id="1e7f8-110">**WscRegisterForChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges)<br/>               | <span data-ttu-id="1e7f8-111">Registriert eine Rückruffunktion, die ausgeführt wird, wenn Windows Security Center (WSC) eine Änderung erkennt, die sich auf die Integrität eines der Sicherheitsanbieter auswirken könnte.</span><span class="sxs-lookup"><span data-stu-id="1e7f8-111">Registers a callback function to be run when Windows Security Center (WSC) detects a change that could affect the health of one of the security providers.</span></span><br/>                    |
| [<span data-ttu-id="1e7f8-112">**Wscunregisterchanges**</span><span class="sxs-lookup"><span data-stu-id="1e7f8-112">**WscUnRegisterChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscunregisterchanges)<br/>                 | <span data-ttu-id="1e7f8-113">Bricht eine Rückruf Registrierung ab, die durch einen Aufrufen der [**wscregisterforchanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) -Funktion durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1e7f8-113">Cancels a callback registration that was made by a call to the [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) function.</span></span><br/>                                               |



 

 

 




