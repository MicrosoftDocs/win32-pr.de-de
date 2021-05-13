---
description: Erweitert das ShellLinkObject-Objekt und unterstützt eine zusätzliche Eigenschaft.
title: IShellLinkDual2-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellLinkDual2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 8a63552c-6bce-4583-8df8-a7f7731b35eb
ms.openlocfilehash: 47dc46d20fc6cf5096a38ccfd1790957f1fdd318
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842641"
---
# <a name="ishelllinkdual2-object"></a><span data-ttu-id="2226a-103">IShellLinkDual2-Objekt</span><span class="sxs-lookup"><span data-stu-id="2226a-103">IShellLinkDual2 object</span></span>

<span data-ttu-id="2226a-104">Erweitert das [**ShellLinkObject-Objekt**](shelllinkobject-object.md) und unterstützt eine zusätzliche Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2226a-104">Extends the [**ShellLinkObject**](shelllinkobject-object.md) object and supports one additional property.</span></span>

## <a name="members"></a><span data-ttu-id="2226a-105">Member</span><span class="sxs-lookup"><span data-stu-id="2226a-105">Members</span></span>

<span data-ttu-id="2226a-106">Das **IShellLinkDual2-Objekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2226a-106">The **IShellLinkDual2** object has these types of members:</span></span>

-   [<span data-ttu-id="2226a-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2226a-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2226a-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2226a-108">Properties</span></span>

<span data-ttu-id="2226a-109">Das **IShellLinkDual2-Objekt** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2226a-109">The **IShellLinkDual2** object has these properties.</span></span>



| <span data-ttu-id="2226a-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2226a-110">Property</span></span>                                            | <span data-ttu-id="2226a-111">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="2226a-111">Access type</span></span>          | <span data-ttu-id="2226a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2226a-112">Description</span></span>                                   |
|:----------------------------------------------------|:---------------------|:----------------------------------------------|
| [<span data-ttu-id="2226a-113">**Ziel**</span><span class="sxs-lookup"><span data-stu-id="2226a-113">**Target**</span></span>](ishelllinkdual2-target.md)<br/> | <span data-ttu-id="2226a-114">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2226a-114">Read-only</span></span><br/> | <span data-ttu-id="2226a-115">Enthält das Ziel des Linkobjekts.</span><span class="sxs-lookup"><span data-stu-id="2226a-115">Contains the link object's target.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2226a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2226a-116">Requirements</span></span>



| <span data-ttu-id="2226a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2226a-117">Requirement</span></span> | <span data-ttu-id="2226a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2226a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2226a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2226a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2226a-120">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2226a-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2226a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2226a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2226a-122">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2226a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2226a-123">Header</span><span class="sxs-lookup"><span data-stu-id="2226a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2226a-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="2226a-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="2226a-125">Idl</span><span class="sxs-lookup"><span data-stu-id="2226a-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2226a-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="2226a-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="2226a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2226a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2226a-128"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="2226a-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




