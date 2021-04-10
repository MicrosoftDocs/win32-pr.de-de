---
description: Enthält Informationen über ein Lokalisier bares Druckformular.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: FORM_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215853"
---
# <a name="form_info_2-structure"></a><span data-ttu-id="cb6c7-103">Formular \_ Info \_ 2-Struktur</span><span class="sxs-lookup"><span data-stu-id="cb6c7-103">FORM\_INFO\_2 structure</span></span>

<span data-ttu-id="cb6c7-104">Enthält Informationen über ein Lokalisier bares Druckformular.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-104">Contains information about a localizable print form.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb6c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb6c7-105">Syntax</span></span>


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a><span data-ttu-id="cb6c7-106">Member</span><span class="sxs-lookup"><span data-stu-id="cb6c7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cb6c7-107">**Flags**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="cb6c7-108">Die Formular Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-108">The form properties.</span></span> <span data-ttu-id="cb6c7-109">Die folgenden Werte sind definiert, aber es kann nur eine festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-109">The following values are defined, but only one can be set.</span></span> <span data-ttu-id="cb6c7-110">Wenn das **Formular \_ Info \_ 2** von [**GetForm**](getform.md) oder [**enumforms**](enumforms.md)zurückgegeben wird, wird **Flags** auf den aktuellen Wert in der Forms-Datenbank festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-110">When the **FORM\_INFO\_2** is returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md), **Flags** is set to the current value in the forms database.</span></span>



| <span data-ttu-id="cb6c7-111">Wert</span><span class="sxs-lookup"><span data-stu-id="cb6c7-111">Value</span></span>         | <span data-ttu-id="cb6c7-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb6c7-112">Meaning</span></span>                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6c7-113">Formular \_ Benutzer</span><span class="sxs-lookup"><span data-stu-id="cb6c7-113">FORM\_USER</span></span>    | <span data-ttu-id="cb6c7-114">Wenn dieses Bitflag festgelegt ist, wurde das Formular vom Benutzer definiert.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-114">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="cb6c7-115">Formulare mit diesem Flagsatz werden in der Registrierung definiert.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-115">Forms with this flag set are defined in the registry.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="cb6c7-116">Formular \_ vordefiniert</span><span class="sxs-lookup"><span data-stu-id="cb6c7-116">FORM\_BUILTIN</span></span> | <span data-ttu-id="cb6c7-117">Wenn dieses Bitflag festgelegt ist, ist das Formular Teil des Spoolers.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-117">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="cb6c7-118">Formular Definitionen mit diesem Flagsatz werden nicht in der Registrierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-118">Form definitions with this flag set do not appear in the registry.</span></span> <span data-ttu-id="cb6c7-119">Integrierte Formulare können nicht geändert werden. Daher sollte dieses Flag nicht festgelegt werden, wenn die Struktur an " [**AddForm**](addform.md) " oder " [**setform**](setform.md)" übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-119">Built-in forms cannot be modified, so this flag should not be set when the structure is passed to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> |
| <span data-ttu-id="cb6c7-120">Formular \_ Drucker</span><span class="sxs-lookup"><span data-stu-id="cb6c7-120">FORM\_PRINTER</span></span> | <span data-ttu-id="cb6c7-121">Wenn dieses Bitflag festgelegt ist, wird das Formular einem bestimmten Drucker zugeordnet, und seine Definition wird in der Registrierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="cb6c7-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="cb6c7-123">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Formulars angibt.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-123">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="cb6c7-124">Der Formular Name darf nicht länger als 31 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="cb6c7-125">**Größe**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="cb6c7-126">Die Breite und Höhe des Formulars in tausendstel Millimeter.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-126">The width and height of the form in thousandths of millimeters.</span></span>

</dd> <dt>

<span data-ttu-id="cb6c7-127">**Imageablearea**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="cb6c7-128">Die Breite und Höhe des Bereichs der Seite, auf der der Drucker drucken kann, in tausendstel Millimeter.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-128">The width and height, in thousandths of millimeters, of the area of the page on which the printer can print.</span></span>

</dd> <dt>

<span data-ttu-id="cb6c7-129">**pkeyword**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-129">**pKeyword**</span></span>
</dt> <dd>

<span data-ttu-id="cb6c7-130">Ein Zeiger auf einen nicht lokalisierbaren Zeichen folgen Bezeichner des Formulars.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-130">A pointer to a non-localizable string identifier of the form.</span></span> <span data-ttu-id="cb6c7-131">Dies ermöglicht es dem Aufrufer, das Formular in allen Gebiets Schemas zu identifizieren, wenn es an [**AddForm**](addform.md) oder [**setform**](setform.md)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-131">When passed to [**AddForm**](addform.md) or [**SetForm**](setform.md), this gives the caller a means of identifying the form in all locales.</span></span>

</dd> <dt>

<span data-ttu-id="cb6c7-132">**StringType**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-132">**StringType**</span></span>
</dt> <dd>

<span data-ttu-id="cb6c7-133">Gibt an, wie ein lokalisierter Anzeige Name für das Formular zur Laufzeit abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-133">Specifies how a localized display name for the form is obtained at runtime.</span></span> <span data-ttu-id="cb6c7-134">Die folgenden Werte sind definiert.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-134">The following values are defined.</span></span> <span data-ttu-id="cb6c7-135">Nur eine kann in einem beliebigen Befehl von [**AddForm**](addform.md) oder [**setform**](setform.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-135">Only one can be set in any given call to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> <span data-ttu-id="cb6c7-136">Sowohl String \_ muidll als auch String \_ langpair können in der **Form \_ Info \_ 2** (s) festgelegt werden, die von [**GetForm**](getform.md) oder [**enumforms**](enumforms.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-136">Both STRING\_MUIDLL and STRING\_LANGPAIR can be set in the **FORM\_INFO\_2** (s) returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md).</span></span> <span data-ttu-id="cb6c7-137">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-137">See Remarks.</span></span>



| <span data-ttu-id="cb6c7-138">Wert</span><span class="sxs-lookup"><span data-stu-id="cb6c7-138">Value</span></span>            | <span data-ttu-id="cb6c7-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb6c7-139">Meaning</span></span>                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6c7-140">Zeichenfolge \_ None</span><span class="sxs-lookup"><span data-stu-id="cb6c7-140">STRING\_NONE</span></span>     | <span data-ttu-id="cb6c7-141">Es ist kein lokalisierter Anzeige Name vorhanden.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-141">There is no localized display name.</span></span>                                                                                                                                                            |
| <span data-ttu-id="cb6c7-142">Zeichenfolge \_ muidll</span><span class="sxs-lookup"><span data-stu-id="cb6c7-142">STRING\_MUIDLL</span></span>   | <span data-ttu-id="cb6c7-143">Der Anzeige Name wird von der in **pmuidll** angegebenen lokalisierten Ressourcen-DLL für die [mehrsprachige Benutzeroberfläche](/windows/desktop/Intl/mui-resource-management) extrahiert.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-143">The display name is extracted from the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resources DLL specified in **pMuiDll**.</span></span> <span data-ttu-id="cb6c7-144">Die ID befindet sich im Member **dwresourceid** .</span><span class="sxs-lookup"><span data-stu-id="cb6c7-144">The ID is in the **dwResourceId** member.</span></span> |
| <span data-ttu-id="cb6c7-145">Zeichenfolge \_ langpair</span><span class="sxs-lookup"><span data-stu-id="cb6c7-145">STRING\_LANGPAIR</span></span> | <span data-ttu-id="cb6c7-146">Der Anzeige Name und die Sprach-ID werden direkt von **pdisplayname** bereitgestellt, und die Sprache wird von **wlangid** angegeben.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-146">The display name and language ID are provided directly by **pDisplayName** and the language is specified by **wLangId**.</span></span>                                                                       |



 

</dd> <dt>

<span data-ttu-id="cb6c7-147">**pmuidll**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-147">**pMuiDll**</span></span>
</dt> <dd>

<span data-ttu-id="cb6c7-148">Die [mehrsprachige Benutzeroberfläche](/windows/desktop/Intl/mui-resource-management) lokalisierte Ressourcen-DLL, die den lokalisierten anzeigen Amen enthält.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-148">The [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resource DLL that contains the localized display name.</span></span>

</dd> <dt>

<span data-ttu-id="cb6c7-149">**dwresourceid**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-149">**dwResourceId**</span></span>
</dt> <dd>

<span data-ttu-id="cb6c7-150">Die Ressourcen-ID für den anzeigen amen des Formulars in **pmuidll**.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-150">The resource ID of the form's display name in **pMuiDll**.</span></span>

</dd> <dt>

<span data-ttu-id="cb6c7-151">**pdisplayname**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-151">**pDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="cb6c7-152">Der Anzeige Name des Formulars in der Sprache, die von **wlangid** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-152">The form's display name in the language specified by **wLangId**.</span></span>

</dd> <dt>

<span data-ttu-id="cb6c7-153">**wlangid**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-153">**wLangId**</span></span>
</dt> <dd>

<span data-ttu-id="cb6c7-154">Die Sprache von **pdisplayname**.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-154">The language of the **pDisplayName**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb6c7-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb6c7-155">Remarks</span></span>

<span data-ttu-id="cb6c7-156">Bei einem Aufrufen von [**AddForm**](addform.md) oder [**setform**](setform.md):</span><span class="sxs-lookup"><span data-stu-id="cb6c7-156">On a call to [**AddForm**](addform.md) or [**SetForm**](setform.md):</span></span>

-   <span data-ttu-id="cb6c7-157">Wenn **StringType** String \_ None ist, müssen sowohl **pmuidll** als auch **pdisplayname** **null** sein, und sowohl **dwresourceid** als auch **wlangid** müssen den Wert 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-157">If **StringType** is STRING\_NONE, both **pMuiDll** and **pDisplayName** must be **NULL** and both **dwResourceId** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="cb6c7-158">Wenn **StringType** String \_ muidll ist, muss **pdisplayname** **null** sein, und **wlangid** muss den Wert 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-158">If **StringType** is STRING\_MUIDLL, **pDisplayName** must be **NULL** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="cb6c7-159">Wenn **StringType** "String \_ langpair" ist, muss **pmuidll** **null** sein, und " **dwresourceid** " muss den Wert "0" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-159">If **StringType** is STRING\_LANGPAIR, **pMuiDll** must be **NULL** and **dwResourceId** must be 0.</span></span>

<span data-ttu-id="cb6c7-160">Für ein **Formular \_ Info \_ 2** , das durch einen [**GetForm**](getform.md) -oder [**enumforms**](enumforms.md)-Rückruf zurückgegeben wird:</span><span class="sxs-lookup"><span data-stu-id="cb6c7-160">For a **FORM\_INFO\_2** returned by a call to [**GetForm**](getform.md) or [**EnumForms**](enumforms.md):</span></span>

-   <span data-ttu-id="cb6c7-161">Wenn **StringType** sowohl String \_ muidll als auch String \_ langpair, **pmuidll**, **pdisplayname**, **dwresourceid** ist, **und wlangid** hat alle gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-161">If **StringType** is both STRING\_MUIDLL and STRING\_LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId**, and **wLangId** will all have valid values.</span></span>
-   <span data-ttu-id="cb6c7-162">Wenn **StringType** nur String \_ muidll ist, verfügen **pmuidll** und **dwresourceid** über gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-162">If **StringType** is STRING\_MUIDLL only, **pMuiDll** and **dwResourceId** will have valid values.</span></span> <span data-ttu-id="cb6c7-163">**pdisplayname** ist **null** , und **wlangid** ist 0.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-163">**pDisplayName** will be **NULL** and **wLangId** will be 0.</span></span>
-   <span data-ttu-id="cb6c7-164">Wenn **StringType** nur String \_ langpair ist, verfügen **pdisplayname** und **wlangid** über gültige Werte.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-164">If **StringType** is STRING\_LANGPAIR only, **pDisplayName** and **wLangId** will have valid values.</span></span> <span data-ttu-id="cb6c7-165">**pmuidll** ist **null** , und **dwresourceid** ist 0.</span><span class="sxs-lookup"><span data-stu-id="cb6c7-165">**pMuiDll** will be **NULL** and **dwResourceId** will be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb6c7-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb6c7-166">Requirements</span></span>



| <span data-ttu-id="cb6c7-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb6c7-167">Requirement</span></span> | <span data-ttu-id="cb6c7-168">Wert</span><span class="sxs-lookup"><span data-stu-id="cb6c7-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6c7-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb6c7-169">Minimum supported client</span></span><br/> | <span data-ttu-id="cb6c7-170">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb6c7-170">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="cb6c7-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb6c7-171">Minimum supported server</span></span><br/> | <span data-ttu-id="cb6c7-172">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb6c7-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cb6c7-173">Header</span><span class="sxs-lookup"><span data-stu-id="cb6c7-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb6c7-174"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb6c7-174"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cb6c7-175">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="cb6c7-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cb6c7-176">**\_ Formular \_ Info \_ 2W** (Unicode) und **\_ Formular \_ Info \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cb6c7-176">**\_FORM\_INFO\_2W** (Unicode) and **\_FORM\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="cb6c7-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb6c7-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb6c7-178">Drucken</span><span class="sxs-lookup"><span data-stu-id="cb6c7-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="cb6c7-179">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="cb6c7-179">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="cb6c7-180">Multilingual User Interface</span><span class="sxs-lookup"><span data-stu-id="cb6c7-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[<span data-ttu-id="cb6c7-181">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-181">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="cb6c7-182">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-182">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="cb6c7-183">**Enumforms**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-183">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="cb6c7-184">**Setform**</span><span class="sxs-lookup"><span data-stu-id="cb6c7-184">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

