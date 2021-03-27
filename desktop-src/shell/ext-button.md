---
description: Enthält Informationen über eine Schaltfläche, die von einer Datei-Manager-Erweiterungs-DLL der Symbolleiste des Datei-Managers hinzugefügt wird.
title: EXT_BUTTON-Struktur (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 5eabb9f5e958b1e0bd15a6412dfbfa276d23f255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751016"
---
# <a name="ext_button-structure"></a><span data-ttu-id="68494-103">Struktur der Ext- \_ Taste</span><span class="sxs-lookup"><span data-stu-id="68494-103">EXT\_BUTTON structure</span></span>

<span data-ttu-id="68494-104">Enthält Informationen über eine Schaltfläche, die von einer Datei-Manager-Erweiterungs-DLL der Symbolleiste des Datei-Managers hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="68494-104">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="68494-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="68494-105">Syntax</span></span>


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a><span data-ttu-id="68494-106">Member</span><span class="sxs-lookup"><span data-stu-id="68494-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="68494-107">**idcommand**</span><span class="sxs-lookup"><span data-stu-id="68494-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="68494-108">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="68494-108">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="68494-109">Ein Befehls Bezeichner für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="68494-109">A command identifier for the button.</span></span>

</dd> <dt>

<span data-ttu-id="68494-110">**idshelp**</span><span class="sxs-lookup"><span data-stu-id="68494-110">**idsHelp**</span></span>
</dt> <dd>

<span data-ttu-id="68494-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="68494-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="68494-112">Der Bezeichner der Hilfe Zeichenfolge für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="68494-112">The identifier of the Help string for the button.</span></span>

</dd> <dt>

<span data-ttu-id="68494-113">**fsstyle**</span><span class="sxs-lookup"><span data-stu-id="68494-113">**fsStyle**</span></span>
</dt> <dd>

<span data-ttu-id="68494-114">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="68494-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="68494-115">Der Stil der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="68494-115">The style of the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68494-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="68494-116">Requirements</span></span>



| <span data-ttu-id="68494-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68494-117">Requirement</span></span> | <span data-ttu-id="68494-118">Wert</span><span class="sxs-lookup"><span data-stu-id="68494-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68494-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68494-119">Minimum supported client</span></span><br/> | <span data-ttu-id="68494-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68494-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="68494-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68494-121">Minimum supported server</span></span><br/> | <span data-ttu-id="68494-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68494-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68494-123">Header</span><span class="sxs-lookup"><span data-stu-id="68494-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="68494-124"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="68494-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68494-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="68494-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68494-126">**"Tool barload" von "f" \_**</span><span class="sxs-lookup"><span data-stu-id="68494-126">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> <dt>

[<span data-ttu-id="68494-127">**f- \_ Toolbar laden**</span><span class="sxs-lookup"><span data-stu-id="68494-127">**FMS\_TOOLBARLOAD**</span></span>](fms-toolbarload.md)
</dt> </dl>

 

 




