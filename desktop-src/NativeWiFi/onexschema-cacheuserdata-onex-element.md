---
description: Gibt an, ob die Benutzer Anmelde Informationen für nachfolgende Verbindungen zwischengespeichert werden.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: cacheuserdata (Onex)-Element
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8650bb2e5899e96f921d57460c8ba49ffab0ea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959652"
---
# <a name="cacheuserdata-onex-element"></a><span data-ttu-id="df12c-103">cacheuserdata (Onex)-Element</span><span class="sxs-lookup"><span data-stu-id="df12c-103">cacheUserData (OneX) Element</span></span>

<span data-ttu-id="df12c-104">Das cacheuserdata (Onex)-Element gibt an, ob die Benutzer Anmelde Informationen für nachfolgende Verbindungen zwischengespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="df12c-104">The cacheUserData (OneX) element specifies whether the user credentials are cached for subsequent connections.</span></span> <span data-ttu-id="df12c-105">Wenn cacheuserdata den Wert true hat, werden die Anmelde Informationen zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="df12c-105">When cacheUserData is TRUE, the credentials are cached.</span></span> <span data-ttu-id="df12c-106">Wenn cacheuserdata den Wert false hat, werden die Anmelde Informationen nicht zwischengespeichert, und der Benutzer wird möglicherweise bei nachfolgenden Verbindungs versuchen zur Eingabe von Anmelde Informationen aufgefordert</span><span class="sxs-lookup"><span data-stu-id="df12c-106">When cacheUserData is FALSE, the credentials are not cached and the user may be prompted for credentials on subsequent connection attempts.</span></span>

<span data-ttu-id="df12c-107">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="df12c-107">This element is optional.</span></span> <span data-ttu-id="df12c-108">Wenn cacheuserdata nicht in einem Profil angegeben ist, werden die Anmelde Informationen des Benutzers zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="df12c-108">When cacheUserData is not specified in a profile, the user credentials are cached.</span></span>

<span data-ttu-id="df12c-109">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Dieses Element wird ignoriert, wenn es in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="df12c-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

<span data-ttu-id="df12c-110">Das **cacheuserdata** -Element wird durch das [**Onex**](onexschema-onex-element.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="df12c-110">The **cacheUserData** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="df12c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df12c-111">Requirements</span></span>



| <span data-ttu-id="df12c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df12c-112">Requirement</span></span> | <span data-ttu-id="df12c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="df12c-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="df12c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df12c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="df12c-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df12c-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="df12c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df12c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="df12c-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df12c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df12c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df12c-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="df12c-119">**Definitions Kontext des Elements im Schema**</span><span class="sxs-lookup"><span data-stu-id="df12c-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="df12c-120">**Onex**</span><span class="sxs-lookup"><span data-stu-id="df12c-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="df12c-121">**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**</span><span class="sxs-lookup"><span data-stu-id="df12c-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="df12c-122">**Onex**</span><span class="sxs-lookup"><span data-stu-id="df12c-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




