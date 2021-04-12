---
description: Gibt an, ob abgelehnte Netzwerke im Assistenten zum Herstellen einer Verbindung mit einem Netzwerk angezeigt werden.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: showdeniednetwork-Element (globalflags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527800"
---
# <a name="showdeniednetwork-globalflags-element"></a><span data-ttu-id="ad90e-103">showdeniednetwork-Element (globalflags)</span><span class="sxs-lookup"><span data-stu-id="ad90e-103">showDeniedNetwork (globalFlags) Element</span></span>

<span data-ttu-id="ad90e-104">Das **showdeniednetwork** (globalflags)-Element gibt an, ob abgelehnte Netzwerke im Assistenten **zum Herstellen einer Verbindung mit einem Netzwerk** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad90e-104">The **showDeniedNetwork** (globalFlags) element specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <span data-ttu-id="ad90e-105">Netzwerke können durch Gruppenrichtlinien oder Benutzereinstellungen verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="ad90e-105">Networks may be denied by group policy or by user settings.</span></span> <span data-ttu-id="ad90e-106">Wenn **showdeniednetwork** den Wert true aufweist, werden abgelehnte Netzwerke im Assistenten **zum Herstellen einer Verbindung mit einem Netzwerk** angezeigt. Andernfalls werden abgelehnte Netzwerke nicht im Assistenten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad90e-106">When **showDeniedNetwork** has a value of TRUE, denied networks appear in the **Connect to a Network** wizard; otherwise, denied networks do not appear in the wizard.</span></span>

<span data-ttu-id="ad90e-107">Dieses Element ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="ad90e-107">This element is mandatory.</span></span> <span data-ttu-id="ad90e-108">Wenn ein Profil vom AutoConfig-Dienst erstellt wird, wird für dieses Element der Standardwert false verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad90e-108">When a profile is created by the AutoConfig service, this element will take the default value of FALSE.</span></span>

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

<span data-ttu-id="ad90e-109">Das **showdeniednetwork** -Element wird durch das [**globalflags**](wlan-policyschema-globalflags-wlanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="ad90e-109">The **showDeniedNetwork** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad90e-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad90e-110">Requirements</span></span>



| <span data-ttu-id="ad90e-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad90e-111">Requirement</span></span> | <span data-ttu-id="ad90e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ad90e-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ad90e-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad90e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ad90e-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad90e-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ad90e-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad90e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ad90e-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad90e-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad90e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad90e-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad90e-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="ad90e-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ad90e-119">**globalflags**</span><span class="sxs-lookup"><span data-stu-id="ad90e-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="ad90e-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="ad90e-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ad90e-121">**globalflags (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="ad90e-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




