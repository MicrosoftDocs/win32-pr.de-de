---
description: Gibt an, ob für den automatischen Konfigurations Dienst für verkabelte Netzwerke die Verwendung von 802.1 x für die Port Authentifizierung erforderlich ist.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Onexerzwungene (Security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e6656238b0745f8bfef9aff5bcb0b80775dd1da2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362592"
---
# <a name="onexenforced-security-element"></a><span data-ttu-id="cef3f-103">Onexerzwungene (Security)-Element</span><span class="sxs-lookup"><span data-stu-id="cef3f-103">OneXEnforced (security) Element</span></span>

<span data-ttu-id="cef3f-104">Das **onexerzwungene** (Security)-Element gibt an, ob für den automatischen Konfigurations Dienst für verkabelte Netzwerke die Verwendung von 802.1 x für die Port Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cef3f-104">The **OneXEnforced** (security) element specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <span data-ttu-id="cef3f-105">Wenn " **onexerzwungene** " den Wert "true" hat, muss der automatische Konfigurations Dienst 802.1 x für die Port Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="cef3f-105">When **OneXEnforced** is TRUE, the automatic configuration service must use 802.1X for port authentication.</span></span> <span data-ttu-id="cef3f-106">Wenn " **onexerzwungene** " den Wert "false" hat, versucht der automatische Konfigurations Dienst, 802.1 x für die Port Authentifizierung zu verwenden. der Dienst wird jedoch auf keine Authentifizierung zurückgreifen, wenn die 802.1 x-Authentifizierung aus irgendeinem Grund fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="cef3f-106">When **OneXEnforced** is FALSE, then the automatic configuration service will attempt to use 802.1X for port authentication, but the service will fall back to no authentication if 802.1X authentication fails for any reason.</span></span>

<span data-ttu-id="cef3f-107">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="cef3f-107">This element is optional.</span></span> <span data-ttu-id="cef3f-108">Der Standardwert ist FALSE.</span><span class="sxs-lookup"><span data-stu-id="cef3f-108">The default value is FALSE.</span></span>

<span data-ttu-id="cef3f-109">Dieses Element hat nur einen sinnvollen Wert, wenn [**onexaktivierte**](lan-profileschema-onexenabled-security-element.md) true ist.</span><span class="sxs-lookup"><span data-stu-id="cef3f-109">This element only has a meaningful value if [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) is TRUE.</span></span> <span data-ttu-id="cef3f-110">Wenn " **onexaktivierte** " den Wert "false" hat, wird der Wert dieses Elements ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cef3f-110">If **OneXEnabled** is FALSE, then the value of this element is ignored.</span></span>

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

<span data-ttu-id="cef3f-111">Das **onexerzwungene** -Element wird durch das [**Security**](lan-profileschema-security-msm-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="cef3f-111">The **OneXEnforced** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef3f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cef3f-112">Requirements</span></span>



| <span data-ttu-id="cef3f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cef3f-113">Requirement</span></span> | <span data-ttu-id="cef3f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cef3f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cef3f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cef3f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cef3f-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cef3f-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cef3f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cef3f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cef3f-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cef3f-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cef3f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cef3f-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="cef3f-120">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="cef3f-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="cef3f-121">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="cef3f-121">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="cef3f-122">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="cef3f-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="cef3f-123">**Sicherheit (MSM)**</span><span class="sxs-lookup"><span data-stu-id="cef3f-123">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




