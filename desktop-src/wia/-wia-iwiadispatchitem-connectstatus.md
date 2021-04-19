---
description: Ruft den Verbindungsstatus des Geräts ab. Diese Eigenschaft gilt nur für Elemente vom Typ Device (root Items). Mögliche Werte sind &\# 0034; verbunden&\# 0034;, &\# 0034; getrennt&\# 0034; oder NULL (wenn diese Eigenschaft nicht für das Element gilt). Schreibgeschützt.
ms.assetid: 44b1713a-5859-4973-8495-e8a67f2344b2
title: Item. connectstatus (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ConnectStatus
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 48e12c35ad98746f5a263680e74a09c814bbc65a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362490"
---
# <a name="itemconnectstatus-property"></a><span data-ttu-id="d2921-106">Item. connectstatus (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d2921-106">Item.ConnectStatus property</span></span>

<span data-ttu-id="d2921-107">Ruft den Verbindungsstatus des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="d2921-107">Retrieves the connection status of the device.</span></span> <span data-ttu-id="d2921-108">Diese Eigenschaft gilt nur für Elemente vom Typ Device (root Items).</span><span class="sxs-lookup"><span data-stu-id="d2921-108">This property applies only to items of type device (root items).</span></span> <span data-ttu-id="d2921-109">Mögliche Werte sind "verbunden", "getrennt" oder **null** (wenn diese Eigenschaft nicht für das Element gilt).</span><span class="sxs-lookup"><span data-stu-id="d2921-109">Possible values are "connected", "disconnected", or **NULL** (if this property does not apply to the item).</span></span> <span data-ttu-id="d2921-110">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d2921-110">Read-only.</span></span>

<span data-ttu-id="d2921-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d2921-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2921-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2921-112">Syntax</span></span>


```JScript
propVal = Item.ConnectStatus
```



## <a name="property-value"></a><span data-ttu-id="d2921-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d2921-113">Property value</span></span>

<span data-ttu-id="d2921-114">Eine Zeichenfolge, die den Verbindungsstatus empfängt.</span><span class="sxs-lookup"><span data-stu-id="d2921-114">String that receives the connection status.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2921-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2921-115">Requirements</span></span>



| <span data-ttu-id="d2921-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2921-116">Requirement</span></span> | <span data-ttu-id="d2921-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d2921-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2921-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2921-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2921-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2921-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2921-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2921-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2921-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2921-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d2921-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d2921-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2921-123"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="d2921-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




