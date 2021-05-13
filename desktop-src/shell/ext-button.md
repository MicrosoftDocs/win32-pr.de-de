---
description: Enthält Informationen zu einer Schaltfläche, die eine Datei-Manager-Erweiterungs-DLL zur Symbolleiste des Datei-Managers hinzufügung.
title: EXT_BUTTON -Struktur (Wfext.h)
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
ms.openlocfilehash: 6d1505ef7b330f0e935136eacaf808da3add8cd8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843151"
---
# <a name="ext_button-structure"></a><span data-ttu-id="49e7a-103">EXT \_ BUTTON-Struktur</span><span class="sxs-lookup"><span data-stu-id="49e7a-103">EXT\_BUTTON structure</span></span>

<span data-ttu-id="49e7a-104">Enthält Informationen zu einer Schaltfläche, die eine Datei-Manager-Erweiterungs-DLL zur Symbolleiste des Datei-Managers hinzufügung.</span><span class="sxs-lookup"><span data-stu-id="49e7a-104">Contains information about a button that a File Manager extension DLL is adding to the toolbar of File Manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e7a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49e7a-105">Syntax</span></span>


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a><span data-ttu-id="49e7a-106">Member</span><span class="sxs-lookup"><span data-stu-id="49e7a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="49e7a-107">**idCommand**</span><span class="sxs-lookup"><span data-stu-id="49e7a-107">**idCommand**</span></span>
</dt> <dd>

<span data-ttu-id="49e7a-108">Typ: **WORD**</span><span class="sxs-lookup"><span data-stu-id="49e7a-108">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="49e7a-109">Ein Befehlsbezeichner für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="49e7a-109">A command identifier for the button.</span></span>

</dd> <dt>

<span data-ttu-id="49e7a-110">**idsHelp**</span><span class="sxs-lookup"><span data-stu-id="49e7a-110">**idsHelp**</span></span>
</dt> <dd>

<span data-ttu-id="49e7a-111">Typ: **WORD**</span><span class="sxs-lookup"><span data-stu-id="49e7a-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="49e7a-112">Der Bezeichner der Hilfezeichenfolge für die Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="49e7a-112">The identifier of the Help string for the button.</span></span>

</dd> <dt>

<span data-ttu-id="49e7a-113">**fsStyle**</span><span class="sxs-lookup"><span data-stu-id="49e7a-113">**fsStyle**</span></span>
</dt> <dd>

<span data-ttu-id="49e7a-114">Typ: **WORD**</span><span class="sxs-lookup"><span data-stu-id="49e7a-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="49e7a-115">Der Stil der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="49e7a-115">The style of the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49e7a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49e7a-116">Requirements</span></span>



| <span data-ttu-id="49e7a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49e7a-117">Requirement</span></span> | <span data-ttu-id="49e7a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="49e7a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="49e7a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49e7a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="49e7a-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49e7a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="49e7a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49e7a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="49e7a-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49e7a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="49e7a-123">Header</span><span class="sxs-lookup"><span data-stu-id="49e7a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="49e7a-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="49e7a-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49e7a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49e7a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e7a-126">**FMEVENT \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="49e7a-126">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> <dt>

[<span data-ttu-id="49e7a-127">**FMS \_ TOOLBARLOAD**</span><span class="sxs-lookup"><span data-stu-id="49e7a-127">**FMS\_TOOLBARLOAD**</span></span>](fms-toolbarload.md)
</dt> </dl>

 

 




