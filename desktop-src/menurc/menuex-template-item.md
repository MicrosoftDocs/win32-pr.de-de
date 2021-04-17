---
title: MENUEX_TEMPLATE_ITEM Struktur
description: Definiert ein Menü Element in einer erweiterten Menüvorlage. Diese Struktur Definition dient lediglich der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: f6e2fd0a-16b8-48e3-8597-341085a7adbd
keywords:
- MENUEX_TEMPLATE_ITEM Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_ITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca1f73d1174590db5948f54f5c51c91a8c65a8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518698"
---
# <a name="menuex_template_item-structure"></a><span data-ttu-id="2c455-105">Menuex- \_ Vorlagen \_ Elementstruktur</span><span class="sxs-lookup"><span data-stu-id="2c455-105">MENUEX\_TEMPLATE\_ITEM structure</span></span>

<span data-ttu-id="2c455-106">Definiert ein Menü Element in einer erweiterten Menüvorlage.</span><span class="sxs-lookup"><span data-stu-id="2c455-106">Defines a menu item in an extended menu template.</span></span> <span data-ttu-id="2c455-107">Diese Struktur Definition dient lediglich der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2c455-107">This structure definition is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c455-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c455-108">Syntax</span></span>

```C++
typedef struct {
  DWORD dwType;
  DWORD dwState;
  UINT  uId;
  WORD  wFlags;
  WCHAR szText[1];
} MENUEX_TEMPLATE_ITEM;
```

## <a name="members"></a><span data-ttu-id="2c455-109">Member</span><span class="sxs-lookup"><span data-stu-id="2c455-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c455-110">**dwType**</span><span class="sxs-lookup"><span data-stu-id="2c455-110">**dwType**</span></span>
</dt> <dd>

<span data-ttu-id="2c455-111">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2c455-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2c455-112">Der Typ des Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="2c455-112">The menu item type.</span></span> <span data-ttu-id="2c455-113">Dieser Member kann eine Kombination der Werte vom Typ (beginnend mit MFT) sein, die mit der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="2c455-113">This member can be a combination of the type (beginning with MFT) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2c455-114">**dwstate**</span><span class="sxs-lookup"><span data-stu-id="2c455-114">**dwState**</span></span>
</dt> <dd>

<span data-ttu-id="2c455-115">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2c455-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="2c455-116">Der Zustand des Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="2c455-116">The menu item state.</span></span> <span data-ttu-id="2c455-117">Dieser Member kann eine Kombination aus den in der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur aufgelisteten Status Werten (beginnend mit MFS) sein.</span><span class="sxs-lookup"><span data-stu-id="2c455-117">This member can be a combination of the state (beginning with MFS) values listed with the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2c455-118">**uId**</span><span class="sxs-lookup"><span data-stu-id="2c455-118">**uId**</span></span>
</dt> <dd>

<span data-ttu-id="2c455-119">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="2c455-119">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="2c455-120">Der Bezeichner des Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="2c455-120">The menu item identifier.</span></span> <span data-ttu-id="2c455-121">Dies ist ein von der Anwendung definierter Wert, der das Menü Element bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2c455-121">This is an application-defined value that identifies the menu item.</span></span> <span data-ttu-id="2c455-122">In einer erweiterten Menü Ressource können Elemente, die Dropdown Menüs oder Untermenüs sowie Befehls Elemente öffnen, über Bezeichner verfügen.</span><span class="sxs-lookup"><span data-stu-id="2c455-122">In an extended menu resource, items that open drop-down menus or submenus as well as command items can have identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="2c455-123">**wFlags**</span><span class="sxs-lookup"><span data-stu-id="2c455-123">**wFlags**</span></span>
</dt> <dd>

<span data-ttu-id="2c455-124">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="2c455-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="2c455-125">Gibt an, ob es sich beim Menü Element um das letzte Element in der Menüleiste, im Dropdown Menü, im Untermenü oder im Kontextmenü handelt und ob es sich um ein Element handelt, das ein Dropdown Menü oder ein Untermenü öffnet.</span><span class="sxs-lookup"><span data-stu-id="2c455-125">Specifies whether the menu item is the last item in the menu bar, drop-down menu, submenu, or shortcut menu and whether it is an item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="2c455-126">Dieser Member kann NULL oder mehr dieser Werte sein.</span><span class="sxs-lookup"><span data-stu-id="2c455-126">This member can be zero or more of these values.</span></span> <span data-ttu-id="2c455-127">Bei 32-Bit-Anwendungen ist dieser Member ein Wort. bei 16-Bit-Anwendungen ist es ein Byte.</span><span class="sxs-lookup"><span data-stu-id="2c455-127">For 32-bit applications, this member is a word; for 16-bit applications, it is a byte.</span></span>

<dt>

<span data-ttu-id="2c455-128">0x80</span><span class="sxs-lookup"><span data-stu-id="2c455-128">0x80</span></span>
</dt> <dd>

<span data-ttu-id="2c455-129">Die Struktur definiert das letzte Menü Element in der Menüleiste, dem Dropdown Menü, dem Untermenü oder dem Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="2c455-129">The structure defines the last menu item in the menu bar, drop-down menu, submenu, or shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="2c455-130">0x01</span><span class="sxs-lookup"><span data-stu-id="2c455-130">0x01</span></span>
</dt> <dd>

<span data-ttu-id="2c455-131">Die-Struktur definiert ein Element, das ein Dropdown Menü oder ein Untermenü öffnet.</span><span class="sxs-lookup"><span data-stu-id="2c455-131">The structure defines a item that opens a drop-down menu or submenu.</span></span> <span data-ttu-id="2c455-132">Nachfolgende Strukturen definieren Menü Elemente im entsprechenden Dropdown Menü oder Untermenü.</span><span class="sxs-lookup"><span data-stu-id="2c455-132">Subsequent structures define menu items in the corresponding drop-down menu or submenu.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2c455-133">**szText**</span><span class="sxs-lookup"><span data-stu-id="2c455-133">**szText**</span></span>
</dt> <dd>

<span data-ttu-id="2c455-134">Typ: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="2c455-134">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="2c455-135">Der Text des Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="2c455-135">The menu item text.</span></span> <span data-ttu-id="2c455-136">Dieser Member ist eine auf NULL endenden Unicode-Zeichenfolge, die an einer Wort Grenze ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="2c455-136">This member is a null-terminated Unicode string, aligned on a word boundary.</span></span> <span data-ttu-id="2c455-137">Die Größe der Menü Element Definition variiert abhängig von der Länge dieser Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2c455-137">The size of the menu item definition varies depending on the length of this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c455-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c455-138">Remarks</span></span>

<span data-ttu-id="2c455-139">Eine erweiterte Menüvorlage besteht aus einer [**menuex- \_ Vorlagen \_ Header**](menuex-template-header.md) Struktur, gefolgt von einer oder mehreren zusammenhängenden **menuex- \_ Vorlagen \_ Element** Strukturen.</span><span class="sxs-lookup"><span data-stu-id="2c455-139">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one or more contiguous **MENUEX\_TEMPLATE\_ITEM** structures.</span></span> <span data-ttu-id="2c455-140">Die **menuex- \_ Vorlagen \_ Element** Strukturen, die eine Variable Länge haben, werden an den **DWORD** -Grenzen ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="2c455-140">The **MENUEX\_TEMPLATE\_ITEM** structures, which are variable in length, are aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="2c455-141">Verwenden Sie die [**loadmenuindirekte**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) -Funktion, um ein Menü aus einer erweiterten Menüvorlage im Arbeitsspeicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2c455-141">To create a menu from an extended menu template in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c455-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c455-142">Requirements</span></span>



| <span data-ttu-id="2c455-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c455-143">Requirement</span></span> | <span data-ttu-id="2c455-144">Wert</span><span class="sxs-lookup"><span data-stu-id="2c455-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2c455-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c455-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2c455-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c455-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2c455-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c455-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2c455-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c455-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2c455-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c455-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c455-150">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2c455-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2c455-151">**Loadmenuindirekte**</span><span class="sxs-lookup"><span data-stu-id="2c455-151">**LoadMenuIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[<span data-ttu-id="2c455-152">**menuex- \_ Vorlagen \_ Header**</span><span class="sxs-lookup"><span data-stu-id="2c455-152">**MENUEX\_TEMPLATE\_HEADER**</span></span>](menuex-template-header.md)
</dt> <dt>

[<span data-ttu-id="2c455-153">**Menuiteminfo zuordnet**</span><span class="sxs-lookup"><span data-stu-id="2c455-153">**MENUITEMINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

<span data-ttu-id="2c455-154">**Licher**</span><span class="sxs-lookup"><span data-stu-id="2c455-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2c455-155">Menüs</span><span class="sxs-lookup"><span data-stu-id="2c455-155">Menus</span></span>](menus.md)
</dt> </dl>

 

 





