---
description: Identifiziert den Namen des Basis Anbieters für das angegebene SIM/Gerät.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Homeprovidername (mbnprofile)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 3d0af51e4873915838f2d55f683d07e9098aad3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751289"
---
# <a name="homeprovidername-mbnprofile-element"></a><span data-ttu-id="0921f-103">Homeprovidername (mbnprofile)-Element</span><span class="sxs-lookup"><span data-stu-id="0921f-103">HomeProviderName (MBNProfile) Element</span></span>

<span data-ttu-id="0921f-104">Das Element **homeprovidername (mbnprofile)** identifiziert den Namen des Home-Anbieters für das angegebene SIM/Gerät.</span><span class="sxs-lookup"><span data-stu-id="0921f-104">The **HomeProviderName (MBNProfile)** element identifies the name of Home provider for the given SIM/Device.</span></span>

<span data-ttu-id="0921f-105">Dieses Element ist optional und wird vom mobilen Breitbanddienst zur internen Verwendung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0921f-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="0921f-106">Eine Anwendung sollte dieses Feld beim Erstellen oder Aktualisieren eines Profils nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="0921f-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

<span data-ttu-id="0921f-107">Das **homeprovidername** -Element wird durch das [**mbnprofile**](schema-mbnprofile-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="0921f-107">The **HomeProviderName** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0921f-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0921f-108">Requirements</span></span>



| <span data-ttu-id="0921f-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0921f-109">Requirement</span></span> | <span data-ttu-id="0921f-110">Wert</span><span class="sxs-lookup"><span data-stu-id="0921f-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="0921f-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0921f-111">Minimum supported client</span></span><br/> | <span data-ttu-id="0921f-112">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="0921f-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="0921f-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0921f-113">Minimum supported server</span></span><br/> | <span data-ttu-id="0921f-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0921f-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="0921f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0921f-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="0921f-116">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="0921f-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0921f-117">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="0921f-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="0921f-118">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="0921f-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0921f-119">**Mbnprofile**</span><span class="sxs-lookup"><span data-stu-id="0921f-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




