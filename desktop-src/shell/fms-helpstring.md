---
description: Enthält Informationen, die der Datei-Manager verwendet, um eine Hilfezeichenfolge für ein Menü- oder Symbolleistenbefehlselement hinzuzufügen.
title: FMS_HELPSTRING-Struktur (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: 4e9521df91619d108c7a03b6574926147fc2b04a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842211"
---
# <a name="fms_helpstring-structure"></a><span data-ttu-id="bd3cf-103">FMS \_ HELPSTRING-Struktur</span><span class="sxs-lookup"><span data-stu-id="bd3cf-103">FMS\_HELPSTRING structure</span></span>

<span data-ttu-id="bd3cf-104">Enthält Informationen, die der Datei-Manager verwendet, um eine Hilfezeichenfolge für ein Menü- oder Symbolleistenbefehlselement hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-104">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd3cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd3cf-105">Syntax</span></span>


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a><span data-ttu-id="bd3cf-106">Member</span><span class="sxs-lookup"><span data-stu-id="bd3cf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bd3cf-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="bd3cf-108">Typ: **INT**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-108">Type: **INT**</span></span>

</dd> <dd>

<span data-ttu-id="bd3cf-109">Der Bezeichner des Befehlselements.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-109">The identifier of the command item.</span></span>

</dd> <dt>

<span data-ttu-id="bd3cf-110">**Hmenu**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-110">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="bd3cf-111">Typ: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-111">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="bd3cf-112">Der Bezeichner der Menüleiste.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-112">The identifier of the menu bar.</span></span>

</dd> <dt>

<span data-ttu-id="bd3cf-113">**szHelp**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-113">**szHelp**</span></span>
</dt> <dd>

<span data-ttu-id="bd3cf-114">Typ: **\_ \_ wchar \_ t \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-114">Type: **\_\_wchar\_t\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="bd3cf-115">Die auf NULL endende Zeichenfolge, die den Hilfetext empfängt.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-115">The null-terminated string that receives the Help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd3cf-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd3cf-116">Requirements</span></span>



| <span data-ttu-id="bd3cf-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd3cf-117">Requirement</span></span> | <span data-ttu-id="bd3cf-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bd3cf-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bd3cf-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd3cf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bd3cf-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bd3cf-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd3cf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bd3cf-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bd3cf-123">Header</span><span class="sxs-lookup"><span data-stu-id="bd3cf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd3cf-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="bd3cf-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd3cf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd3cf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd3cf-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="bd3cf-127">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-127">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




