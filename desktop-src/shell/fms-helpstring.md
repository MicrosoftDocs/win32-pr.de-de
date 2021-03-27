---
description: Enthält Informationen, die der Datei-Manager verwendet, um eine Hilfe Zeichenfolge für ein Menü oder Symbolleisten-Befehls Element hinzuzufügen
title: FMS_HELPSTRING-Struktur (WF. h)
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
ms.openlocfilehash: c934409712ae740797eb3b5af0b55c50ff125342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994742"
---
# <a name="fms_helpstring-structure"></a><span data-ttu-id="f378f-103">Struktur von "Help String" in f \_</span><span class="sxs-lookup"><span data-stu-id="f378f-103">FMS\_HELPSTRING structure</span></span>

<span data-ttu-id="f378f-104">Enthält Informationen, die der Datei-Manager verwendet, um eine Hilfe Zeichenfolge für ein Menü oder Symbolleisten-Befehls Element hinzuzufügen</span><span class="sxs-lookup"><span data-stu-id="f378f-104">Contains information that File Manager uses to add a Help string for a menu or toolbar command item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f378f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f378f-105">Syntax</span></span>


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a><span data-ttu-id="f378f-106">Member</span><span class="sxs-lookup"><span data-stu-id="f378f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f378f-107">**idcommand**</span><span class="sxs-lookup"><span data-stu-id="f378f-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="f378f-108">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="f378f-108">Type: **INT**</span></span>

</dd> <dd>

<span data-ttu-id="f378f-109">Der Bezeichner des Befehls Elements.</span><span class="sxs-lookup"><span data-stu-id="f378f-109">The identifier of the command item.</span></span>

</dd> <dt>

<span data-ttu-id="f378f-110">**HMENU**</span><span class="sxs-lookup"><span data-stu-id="f378f-110">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="f378f-111">Typ: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="f378f-111">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="f378f-112">Der Bezeichner der Menüleiste.</span><span class="sxs-lookup"><span data-stu-id="f378f-112">The identifier of the menu bar.</span></span>

</dd> <dt>

<span data-ttu-id="f378f-113">**szhelp**</span><span class="sxs-lookup"><span data-stu-id="f378f-113">**szHelp**</span></span>
</dt> <dd>

<span data-ttu-id="f378f-114">Typ: **\_ \_ WCHAR \_ t \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="f378f-114">Type: **\_\_wchar\_t\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="f378f-115">Die NULL-terminierte Zeichenfolge, die den Hilfetext empfängt.</span><span class="sxs-lookup"><span data-stu-id="f378f-115">The null-terminated string that receives the Help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f378f-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f378f-116">Requirements</span></span>



| <span data-ttu-id="f378f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f378f-117">Requirement</span></span> | <span data-ttu-id="f378f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f378f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f378f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f378f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f378f-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f378f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f378f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f378f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f378f-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f378f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f378f-123">Header</span><span class="sxs-lookup"><span data-stu-id="f378f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f378f-124"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="f378f-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f378f-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f378f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f378f-126">**"F"**</span><span class="sxs-lookup"><span data-stu-id="f378f-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="f378f-127">**"helpmenuitem" für "f" \_**</span><span class="sxs-lookup"><span data-stu-id="f378f-127">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




