---
description: Gibt an, ob der Dienst für die automatische Konfiguration von Kabel Netzwerken mithilfe von 802.1 x eine Port Authentifizierung durchführen soll.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Onexaktiviertes (Security)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c76fce3b42cff648d03f520ddeb569a39e99f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216923"
---
# <a name="onexenabled-security-element"></a><span data-ttu-id="674aa-103">Onexaktiviertes (Security)-Element</span><span class="sxs-lookup"><span data-stu-id="674aa-103">OneXEnabled (security) Element</span></span>

<span data-ttu-id="674aa-104">Das **onexaktivierte** (Security)-Element gibt an, ob der automatische Konfigurations Dienst für verkabelte Netzwerke mithilfe von 802.1 x eine Port Authentifizierung durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="674aa-104">The **OneXEnabled** (security) element specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <span data-ttu-id="674aa-105">Wenn " **onexaktivierte** " den Wert "false" hat, verwendet der automatische Konfigurations Dienst 802.1 x nie für die Port Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="674aa-105">When **OneXEnabled** is FALSE, the automatic configuration service never uses 802.1X for port authentication.</span></span> <span data-ttu-id="674aa-106">Wenn " **onexaktivierte** " den Wert "true" hat, versucht der automatische Konfigurations Dienst mithilfe von 802.1 x die Port Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="674aa-106">When **OneXEnabled** is TRUE, then the automatic configuration service attempts port authentication using 802.1X.</span></span>

<span data-ttu-id="674aa-107">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="674aa-107">This element is optional.</span></span> <span data-ttu-id="674aa-108">Der Standardwert ist TRUE.</span><span class="sxs-lookup"><span data-stu-id="674aa-108">The default value is TRUE.</span></span> <span data-ttu-id="674aa-109">Wenn **onexused** nicht in einem Profil angegeben ist, kann 802.1 x für die Port Authentifizierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="674aa-109">When **OneXEnabled** is not specified in a profile, then 802.1X may be used for port authentication.</span></span>

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

<span data-ttu-id="674aa-110">Das **onexaktivierte** -Element wird durch das [**Security**](lan-profileschema-security-msm-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="674aa-110">The **OneXEnabled** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="674aa-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="674aa-111">Requirements</span></span>



| <span data-ttu-id="674aa-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="674aa-112">Requirement</span></span> | <span data-ttu-id="674aa-113">Wert</span><span class="sxs-lookup"><span data-stu-id="674aa-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="674aa-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="674aa-114">Minimum supported client</span></span><br/> | <span data-ttu-id="674aa-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="674aa-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="674aa-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="674aa-116">Minimum supported server</span></span><br/> | <span data-ttu-id="674aa-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="674aa-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="674aa-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="674aa-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="674aa-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="674aa-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="674aa-120">**Sicherung**</span><span class="sxs-lookup"><span data-stu-id="674aa-120">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="674aa-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="674aa-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="674aa-122">**Sicherheit (MSM)**</span><span class="sxs-lookup"><span data-stu-id="674aa-122">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




