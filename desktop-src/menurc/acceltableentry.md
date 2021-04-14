---
title: Acceltableentry-Struktur
description: Beschreibt die Daten in einer einzelnen Zugriffstasten-Tabellen Ressource. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 510594ae-56ea-49fb-abd3-ec06e51f2e0e
keywords:
- Acceltableentry-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- ACCELTABLEENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ff12fe39f2ea54c90530133263bceb157d79dcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479083"
---
# <a name="acceltableentry-structure"></a><span data-ttu-id="39825-105">Acceltableentry-Struktur</span><span class="sxs-lookup"><span data-stu-id="39825-105">ACCELTABLEENTRY structure</span></span>

<span data-ttu-id="39825-106">Beschreibt die Daten in einer einzelnen Zugriffstasten-Tabellen Ressource.</span><span class="sxs-lookup"><span data-stu-id="39825-106">Describes the data in an individual accelerator table resource.</span></span> <span data-ttu-id="39825-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="39825-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="39825-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="39825-108">Syntax</span></span>


```C++
typedef struct {
  WORD fFlags;
  WORD wAnsi;
  WORD wId;
  WORD padding;
} ACCELTABLEENTRY;
```



## <a name="members"></a><span data-ttu-id="39825-109">Member</span><span class="sxs-lookup"><span data-stu-id="39825-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="39825-110">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="39825-110">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="39825-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="39825-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="39825-112">Beschreibt die Eigenschaften der Tastatur Beschleunigung.</span><span class="sxs-lookup"><span data-stu-id="39825-112">Describes keyboard accelerator characteristics.</span></span> <span data-ttu-id="39825-113">Dieser Member kann einen oder mehrere der folgenden Werte aus "Winuser. h" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="39825-113">This member can have one or more of the following values from Winuser.h.</span></span>



| <span data-ttu-id="39825-114">Wert</span><span class="sxs-lookup"><span data-stu-id="39825-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="39825-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="39825-115">Meaning</span></span>                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVIRTKEY"></span><span id="fvirtkey"></span><dl> <span data-ttu-id="39825-116">" <dt>**evirtkey**</dt> " <dt>true</dt></span><span class="sxs-lookup"><span data-stu-id="39825-116"><dt>**FVIRTKEY**</dt> <dt>TRUE</dt></span></span> </dl>    | <span data-ttu-id="39825-117">Die Zugriffstaste ist ein Code, der aus dem [virtuellen Schlüssel](/windows/desktop/inputdev/virtual-key-codes)besteht.</span><span class="sxs-lookup"><span data-stu-id="39825-117">The accelerator key is a [virtual-key code](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="39825-118">Wenn dieses Flag nicht angegeben wird, wird davon ausgegangen, dass die Zugriffstaste einen ASCII-Zeichencode angibt.</span><span class="sxs-lookup"><span data-stu-id="39825-118">If this flag is not specified, the accelerator key is assumed to specify an ASCII character code.</span></span> <br/>                          |
| <span id="FNOINVERT"></span><span id="fnoinvert"></span><dl> <span data-ttu-id="39825-119"><dt>**Spnoinvert**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="39825-119"><dt>**FNOINVERT**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="39825-120">Ein Menü Element in der Menüleiste wird nicht hervorgehoben, wenn eine Zugriffstaste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39825-120">A menu item on the menu bar is not highlighted when an accelerator is used.</span></span> <span data-ttu-id="39825-121">Dieses Attribut ist veraltet und wird nur aus Gründen der Abwärtskompatibilität mit Ressourcen Dateien, die für 16-Bit-Windows entwickelt wurden, beibehalten.</span><span class="sxs-lookup"><span data-stu-id="39825-121">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span><br/> |
| <span id="FSHIFT"></span><span id="fshift"></span><dl> <span data-ttu-id="39825-122"><dt>**F**</dt> -Taste <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="39825-122"><dt>**FSHIFT**</dt> <dt>0x04</dt></span></span> </dl>          | <span data-ttu-id="39825-123">Die Zugriffstaste wird nur aktiviert, wenn der Benutzer die UMSCHALTTASTE drückt.</span><span class="sxs-lookup"><span data-stu-id="39825-123">The accelerator is activated only if the user presses the SHIFT key.</span></span> <span data-ttu-id="39825-124">Dieses Flag gilt nur für virtuelle Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="39825-124">This flag applies only to virtual keys.</span></span> <br/>                                                                                        |
| <span id="FCONTROL"></span><span id="fcontrol"></span><dl> <span data-ttu-id="39825-125"><dt>**Steuerelement**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="39825-125"><dt>**FCONTROL**</dt> <dt>0x08</dt></span></span> </dl>    | <span data-ttu-id="39825-126">Die Zugriffstaste wird nur aktiviert, wenn der Benutzer die STRG-Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="39825-126">The accelerator is activated only if the user presses the CTRL key.</span></span> <span data-ttu-id="39825-127">Dieses Flag gilt nur für virtuelle Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="39825-127">This flag applies only to virtual keys.</span></span> <br/>                                                                                         |
| <span id="FALT"></span><span id="falt"></span><dl> <span data-ttu-id="39825-128"><dt></dt> - <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="39825-128"><dt>**FALT**</dt> <dt>0x10</dt></span></span> </dl>                | <span data-ttu-id="39825-129">Die Zugriffstaste wird nur aktiviert, wenn der Benutzer die Alt-Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="39825-129">The accelerator is activated only if the user presses the ALT key.</span></span> <span data-ttu-id="39825-130">Dieses Flag gilt nur für virtuelle Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="39825-130">This flag applies only to virtual keys.</span></span> <br/>                                                                                          |
| <span id="0x80"></span><span id="0X80"></span><dl> <span data-ttu-id="39825-131"><dt>**0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="39825-131"><dt>**0x80**</dt></span></span> </dl>                                                                          | <span data-ttu-id="39825-132">Der Eintrag ist zuletzt in einer Zugriffstasten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="39825-132">The entry is last in an accelerator table.</span></span> <br/>                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="39825-133">**wansi**</span><span class="sxs-lookup"><span data-stu-id="39825-133">**wAnsi**</span></span>
</dt> <dd>

<span data-ttu-id="39825-134">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="39825-134">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="39825-135">Ein ANSI-Zeichen Wert oder ein Code für den virtuellen Schlüssel, der die Zugriffstaste identifiziert.</span><span class="sxs-lookup"><span data-stu-id="39825-135">An ANSI character value or a virtual-key code that identifies the accelerator key.</span></span>

</dd> <dt>

<span data-ttu-id="39825-136">**wId**</span><span class="sxs-lookup"><span data-stu-id="39825-136">**wId**</span></span>
</dt> <dd>

<span data-ttu-id="39825-137">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="39825-137">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="39825-138">Ein Bezeichner für die Tastatur Beschleunigung.</span><span class="sxs-lookup"><span data-stu-id="39825-138">An identifier for the keyboard accelerator.</span></span> <span data-ttu-id="39825-139">Dies ist der Wert, der an die Fenster Prozedur übermittelt wird, wenn der Benutzer den angegebenen Schlüssel drückt.</span><span class="sxs-lookup"><span data-stu-id="39825-139">This is the value passed to the window procedure when the user presses the specified key.</span></span>

</dd> <dt>

<span data-ttu-id="39825-140">**padding**</span><span class="sxs-lookup"><span data-stu-id="39825-140">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="39825-141">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="39825-141">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="39825-142">Die Anzahl der eingefügten bytes, um sicherzustellen, dass die Struktur an einer **DWORD** -Grenze ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="39825-142">The number of bytes inserted to ensure that the structure is aligned on a **DWORD** boundary.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39825-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39825-143">Remarks</span></span>

<span data-ttu-id="39825-144">Die **acceltableentry** -Struktur wird für alle Zugriffstasten Tabelleneinträge in der Ressource wiederholt.</span><span class="sxs-lookup"><span data-stu-id="39825-144">The **ACCELTABLEENTRY** structure is repeated for all accelerator table entries in the resource.</span></span> <span data-ttu-id="39825-145">Der letzte Eintrag in der Tabelle wird mit dem Wert 0x0080 gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="39825-145">The last entry in the table is flagged with the value 0x0080.</span></span>

<span data-ttu-id="39825-146">Sie können die Anzahl der Elemente in der Tabelle berechnen, wenn Sie die Länge der Ressource um acht aufteilen.</span><span class="sxs-lookup"><span data-stu-id="39825-146">You can compute the number of elements in the table if you divide the length of the resource by eight.</span></span> <span data-ttu-id="39825-147">Anschließend kann die Anwendung nach dem Zufallsprinzip auf die einzelnen Einträge fester Länge zugreifen.</span><span class="sxs-lookup"><span data-stu-id="39825-147">Then your application can randomly access the individual fixed-length entries.</span></span>

## <a name="requirements"></a><span data-ttu-id="39825-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39825-148">Requirements</span></span>



| <span data-ttu-id="39825-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39825-149">Requirement</span></span> | <span data-ttu-id="39825-150">Wert</span><span class="sxs-lookup"><span data-stu-id="39825-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="39825-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39825-151">Minimum supported client</span></span><br/> | <span data-ttu-id="39825-152">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39825-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="39825-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39825-153">Minimum supported server</span></span><br/> | <span data-ttu-id="39825-154">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39825-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="39825-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39825-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="39825-156">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="39825-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="39825-157">**"Kreateacceleratortable"**</span><span class="sxs-lookup"><span data-stu-id="39825-157">**CreateAcceleratorTable**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)
</dt> <dt>

<span data-ttu-id="39825-158">**Licher**</span><span class="sxs-lookup"><span data-stu-id="39825-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="39825-159">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="39825-159">Resources</span></span>](resources.md)
</dt> </dl>

 

