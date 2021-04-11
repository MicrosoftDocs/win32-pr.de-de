---
description: Ein undurchsichtiger Datentyp.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (ntsecpkg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216207"
---
# <a name="plsa_client_request"></a><span data-ttu-id="ca8bf-103">plsa- \_ Client \_ Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca8bf-103">PLSA\_CLIENT\_REQUEST</span></span>

<span data-ttu-id="ca8bf-104">Der Datentyp der **plsa- \_ Client \_ Anforderung** ist ein undurchsichtiger Datentyp.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-104">The **PLSA\_CLIENT\_REQUEST** data type is an opaque data type.</span></span>

<span data-ttu-id="ca8bf-105">Die [*Lokale Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) verwendet diese intern, um Client Informationen zu einzelnen Anforderungen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ca8bf-105">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) uses it internally to maintain client information related to individual requests.</span></span>


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a><span data-ttu-id="ca8bf-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca8bf-106">Requirements</span></span>



| <span data-ttu-id="ca8bf-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca8bf-107">Requirement</span></span> | <span data-ttu-id="ca8bf-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ca8bf-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8bf-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-109">Minimum supported client</span></span><br/> | <span data-ttu-id="ca8bf-110">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca8bf-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ca8bf-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca8bf-111">Minimum supported server</span></span><br/> | <span data-ttu-id="ca8bf-112">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca8bf-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca8bf-113">Header</span><span class="sxs-lookup"><span data-stu-id="ca8bf-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca8bf-114"><dt>Ntsecpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca8bf-114"><dt>Ntsecpkg.h</dt></span></span> </dl> |



 

 
