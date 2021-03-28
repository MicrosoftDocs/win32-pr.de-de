---
description: Enthält Informationen, die der Datei-Manager zum Hinzufügen eines benutzerdefinierten Menüs verwendet, das von einer Datei-Manager-Erweiterungs-DLL Die Struktur bietet auch einen Delta Wert, den die Erweiterungs-DLL verwenden kann, um das benutzerdefinierte Menü zu bearbeiten, nachdem der Datei-Manager das Menü geladen hat.
title: FMS_LOAD-Struktur (WF. h)
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
ms.openlocfilehash: 1745c4e34ac124e9990602350db6479ce287be8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977088"
---
# <a name="fms_load-structure"></a><span data-ttu-id="26011-104">Struktur zum \_ Laden von Strukturen</span><span class="sxs-lookup"><span data-stu-id="26011-104">FMS\_LOAD structure</span></span>

<span data-ttu-id="26011-105">Enthält Informationen, die der Datei-Manager zum Hinzufügen eines benutzerdefinierten Menüs verwendet, das von einer Datei-Manager-Erweiterungs-DLL</span><span class="sxs-lookup"><span data-stu-id="26011-105">Contains information that File Manager uses to add a custom menu provided by a File Manager extension DLL.</span></span> <span data-ttu-id="26011-106">Die Struktur bietet auch einen Delta Wert, den die Erweiterungs-DLL verwenden kann, um das benutzerdefinierte Menü zu bearbeiten, nachdem der Datei-Manager das Menü geladen hat.</span><span class="sxs-lookup"><span data-stu-id="26011-106">The structure also provides a delta value that the extension DLL can use to manipulate the custom menu after File Manager has loaded the menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="26011-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="26011-107">Syntax</span></span>


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a><span data-ttu-id="26011-108">Member</span><span class="sxs-lookup"><span data-stu-id="26011-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="26011-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="26011-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="26011-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="26011-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="26011-111">Die Länge der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="26011-111">The length, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="26011-112">**szmenuname**</span><span class="sxs-lookup"><span data-stu-id="26011-112">**szMenuName**</span></span>
</dt> <dd>

<span data-ttu-id="26011-113">Typ: **TCHAR \[ - \_ Menü \_ Text \] len**</span><span class="sxs-lookup"><span data-stu-id="26011-113">Type: **TCHAR\[MENU\_TEXT\_LEN\]**</span></span>

</dd> <dd>

<span data-ttu-id="26011-114">Ein mit NULL endender Name für ein Menü Element, das in der Menüleiste im Datei-Manager angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="26011-114">A null-terminated name for a menu item that appears on the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="26011-115">**HMENU**</span><span class="sxs-lookup"><span data-stu-id="26011-115">**hMenu**</span></span>
</dt> <dd>

<span data-ttu-id="26011-116">Typ: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="26011-116">Type: **HMENU**</span></span>

</dd> <dd>

<span data-ttu-id="26011-117">Der Bezeichner des Popup Menüs, das der Menüleiste im Datei-Manager hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="26011-117">The identifier of the pop-up menu added to the menu bar in File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="26011-118">**wmenudelta**</span><span class="sxs-lookup"><span data-stu-id="26011-118">**wMenuDelta**</span></span>
</dt> <dd>

<span data-ttu-id="26011-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="26011-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="26011-120">Der Delta Wert des Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="26011-120">The menu item delta value.</span></span> <span data-ttu-id="26011-121">Um Konflikte mit den eigenen Menü Elementen zu vermeiden, benennt der Datei-Manager die Menü Element Bezeichner in dem Popup Menü um, das durch den **HMENU** -Member identifiziert wird, indem dieser Delta Wert den einzelnen Bezeichnern hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="26011-121">To avoid conflicts with its own menu items, File Manager renumbers the menu item identifiers in the pop-up menu identified by the **hMenu** member by adding this delta value to each identifier.</span></span> <span data-ttu-id="26011-122">Eine Erweiterungs-DLL, die ein Menü Element ändern muss, muss das Element identifizieren, indem der Delta Wert dem Bezeichner des Menü Elements hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="26011-122">An extension DLL that must modify a menu item must identify the item by adding the delta value to the menu item's identifier.</span></span> <span data-ttu-id="26011-123">Der Wert dieses Members kann von Sitzung zu Sitzung abweichen.</span><span class="sxs-lookup"><span data-stu-id="26011-123">The value of this member can vary from session to session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26011-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="26011-124">Requirements</span></span>



| <span data-ttu-id="26011-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26011-125">Requirement</span></span> | <span data-ttu-id="26011-126">Wert</span><span class="sxs-lookup"><span data-stu-id="26011-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26011-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26011-127">Minimum supported client</span></span><br/> | <span data-ttu-id="26011-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26011-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="26011-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26011-129">Minimum supported server</span></span><br/> | <span data-ttu-id="26011-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26011-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="26011-131">Header</span><span class="sxs-lookup"><span data-stu-id="26011-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="26011-132"><dt>WF. h</dt></span><span class="sxs-lookup"><span data-stu-id="26011-132"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26011-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="26011-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26011-134">**"F"**</span><span class="sxs-lookup"><span data-stu-id="26011-134">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




