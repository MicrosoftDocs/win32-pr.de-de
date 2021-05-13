---
description: Enthält Informationen, die der Datei-Manager verwendet, um ein benutzerdefiniertes Menü hinzuzufügen, das von einer Datei-Manager-Erweiterungs-DLL bereitgestellt wird. Die -Struktur bietet auch einen Deltawert, den die Erweiterungs-DLL verwenden kann, um das benutzerdefinierte Menü zu bearbeiten, nachdem der Datei-Manager das Menü geladen hat.
title: FMS_LOAD -Struktur (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: efd1777704c775db84c7dabf54b9e06c81535fb4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842191"
---
# <a name="fms_load-structure"></a><span data-ttu-id="0282a-104">FMS \_ LOAD-Struktur</span><span class="sxs-lookup"><span data-stu-id="0282a-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="0282a-105">Enthält Informationen, die der Datei-Manager verwendet, um ein benutzerdefiniertes Menü hinzuzufügen, das von einer Datei-Manager-Erweiterungs-DLL bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0282a-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="0282a-106">Die -Struktur bietet auch einen Deltawert, den die Erweiterungs-DLL verwenden kann, um das benutzerdefinierte Menü zu bearbeiten, nachdem der Datei-Manager das Menü geladen hat.</span><span class="sxs-lookup"><span data-stu-id="0282a-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="0282a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0282a-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="0282a-108">Member</span><span class="sxs-lookup"><span data-stu-id="0282a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0282a-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="0282a-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="0282a-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0282a-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0282a-111">Die Länge der -Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0282a-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="0282a-112">**szMenuName**</span><span class="sxs-lookup"><span data-stu-id="0282a-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="0282a-113">Typ: **TCHAR \[ MENU TEXT \_ \_ LEN \]**</span><span class="sxs-lookup"><span data-stu-id="0282a-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="0282a-114">Ein mit NULL beendeter Name für ein Menüelement, das in der Menüleiste im Datei-Manager angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0282a-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="0282a-115">**Hmenu**</span><span class="sxs-lookup"><span data-stu-id="0282a-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="0282a-116">Typ: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="0282a-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="0282a-117">Der Bezeichner des Popupmenüs, das der Menüleiste im Datei-Manager hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="0282a-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="0282a-118">**wMenuDelta**</span><span class="sxs-lookup"><span data-stu-id="0282a-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="0282a-119">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="0282a-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="0282a-120">Der Deltawert des Menüelements.</span><span class="sxs-lookup"><span data-stu-id="0282a-120">The menu item delta value.</span></span> <span data-ttu-id="0282a-121">Um Konflikte mit eigenen Menüelementen zu vermeiden, nummeriert der Datei-Manager die Menüelementbezeichner im Popupmenü, das vom **hMenu-Element** identifiziert wird, neu, indem dieser Deltawert jedem Bezeichner hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0282a-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="0282a-122">Eine Erweiterungs-DLL, die ein Menüelement ändern muss, muss das Element identifizieren, indem der Deltawert dem Bezeichner des Menüelements hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0282a-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="0282a-123">Der Wert dieses Members kann von Sitzung zu Sitzung variieren.</span><span class="sxs-lookup"><span data-stu-id="0282a-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0282a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0282a-124">Requirements</span></span>



| <span data-ttu-id="0282a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0282a-125">Requirement</span></span> | <span data-ttu-id="0282a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0282a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0282a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0282a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0282a-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0282a-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0282a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0282a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0282a-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0282a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0282a-131">Header</span><span class="sxs-lookup"><span data-stu-id="0282a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0282a-132"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="0282a-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0282a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0282a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0282a-134">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="0282a-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




