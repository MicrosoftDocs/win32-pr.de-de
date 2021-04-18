---
description: Gibt an, ob Computer den integrierten automatischen Konfigurations Dienst (AutoConfig) zum Verwalten von Drahtlos Verbindungen verwenden.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: enableautoconfig (globalflags)-Element (LAN_policy) für WLAN
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
ms.openlocfilehash: 5105b8e634aa5affa8648b763a82bbd60cbaec17
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106364581"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a><span data-ttu-id="fc785-103">enableautoconfig (globalflags)-Element (LAN_policy) für WLAN</span><span class="sxs-lookup"><span data-stu-id="fc785-103">enableAutoConfig (globalFlags) Element (LAN_policy) for WLAN</span></span> 

<span data-ttu-id="fc785-104">Das **enableautoconfig** (globalflags)-Element gibt an, ob Computer den integrierten automatischen Konfigurations Dienst (AutoConfig) zum Verwalten von Drahtlos Verbindungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc785-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <span data-ttu-id="fc785-105">Wenn **enableautoconfig** den Wert false aufweist, dürfen Computer keine automatische Konfiguration zum Verwalten von Drahtlos Verbindungen verwenden, und der Auto Config-Dienst antwortet nur auf Anforderungen zum Aktivieren des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="fc785-105">When **enableAutoConfig** has a value of FALSE, machines must not use AutoConfig to manage wireless connections, and the AutoConfig service only responds to requests to enable the service.</span></span> <span data-ttu-id="fc785-106">Wenn **enableautoconfig** den Wert true aufweist, kann der AutoConfig-Dienst von Computern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc785-106">When **enableAutoConfig** has a value of TRUE, machines may use the AutoConfig service.</span></span>

<span data-ttu-id="fc785-107">Dieses Element ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="fc785-107">This element is mandatory.</span></span> <span data-ttu-id="fc785-108">Wenn ein Profil vom AutoConfig-Dienst erstellt wird, hat dieses Element den Standardwert true.</span><span class="sxs-lookup"><span data-stu-id="fc785-108">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="fc785-109">Das **enableautoconfig** -Element wird durch das [**globalflags**](wlan-policyschema-globalflags-wlanpolicy-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="fc785-109">The **enableAutoConfig** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc785-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc785-110">Requirements</span></span>



| <span data-ttu-id="fc785-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc785-111">Requirement</span></span> | <span data-ttu-id="fc785-112">Wert</span><span class="sxs-lookup"><span data-stu-id="fc785-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc785-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc785-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fc785-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc785-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fc785-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc785-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fc785-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc785-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc785-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc785-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="fc785-118">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="fc785-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fc785-119">**globalflags**</span><span class="sxs-lookup"><span data-stu-id="fc785-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="fc785-120">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="fc785-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fc785-121">**globalflags (wlanpolicy)**</span><span class="sxs-lookup"><span data-stu-id="fc785-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




