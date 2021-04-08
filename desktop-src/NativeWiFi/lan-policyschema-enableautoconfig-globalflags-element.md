---
description: Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst zum Verwalten von Verbindungen mit verkabelten Netzwerken verwenden, die Layer 2-Authentifizierung erfordern (z. b. 802.1 x).
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: enableautoconfig (globalflags)-Element (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757800"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a><span data-ttu-id="d9dfa-103">enableautoconfig (globalflags)-Element (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="d9dfa-103">enableAutoConfig (globalFlags) Element (LAN_policy)</span></span>

<span data-ttu-id="d9dfa-104">Das **enableautoconfig** (globalflags)-Element gibt an, ob Computer den integrierten automatischen Konfigurations Dienst zum Verwalten von Verbindungen mit Kabel Netzwerken verwenden, die Layer 2-Authentifizierung erfordern (z. b. 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="d9dfa-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span>

<span data-ttu-id="d9dfa-105">Wenn **enableautoconfig** den Wert false aufweist, dürfen Computer den integrierten automatischen Konfigurations Dienst nicht zum Verwalten von Verbindungen verwenden, für die die Layer 2-Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-105">When **enableAutoConfig** has a value of FALSE, machines must not use built-in automatic configuration service to manage connections that require layer 2 authentication.</span></span> <span data-ttu-id="d9dfa-106">Stattdessen ist das im [**ProfileList**](lan-policyschema-profilelist-lanpolicy-element.md) -Element angegebene Netzwerk das einzige Netzwerk, das für die Verbindung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-106">Instead, the network specified in the [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) element is the only network available for connection.</span></span> <span data-ttu-id="d9dfa-107">Der Dienst für die automatische Konfiguration antwortet nur auf Anforderungen, um den Dienst zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-107">The automatic configuration service will only respond to requests to enable the service.</span></span>

<span data-ttu-id="d9dfa-108">Wenn **enableautoconfig** den Wert true aufweist, können Computer den integrierten automatischen Konfigurations Dienst verwenden, um eine Verbindung mit Kabel Netzwerken herzustellen, für die Layer 2-Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-108">When **enableAutoConfig** has a value of TRUE, machines may use the built-in automatic configuration service to connect to wired networks that require layer 2 authentication.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="d9dfa-109">Das **enableautoconfig** -Element wird durch das [**globalflags**](lan-policyschema-globalflags-lanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="d9dfa-109">The **enableAutoConfig** element is defined by the [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9dfa-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9dfa-110">Requirements</span></span>



| <span data-ttu-id="d9dfa-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9dfa-111">Requirement</span></span> | <span data-ttu-id="d9dfa-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d9dfa-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d9dfa-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9dfa-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d9dfa-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9dfa-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d9dfa-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9dfa-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d9dfa-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9dfa-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9dfa-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9dfa-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9dfa-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="d9dfa-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d9dfa-119">**globalflags**</span><span class="sxs-lookup"><span data-stu-id="d9dfa-119">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="d9dfa-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="d9dfa-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d9dfa-121">**globalflags (lanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="d9dfa-121">**globalFlags (LANPolicy)**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




