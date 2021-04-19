---
description: Die FORM_INFO_1-Struktur enthält Informationen zu einem Druckformular. Die Informationen umfassen den Ursprung der Druckformulare, den Namen, die Dimensionen und die Dimensionen des druckbaren Bereichs.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: FORM_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373125"
---
# <a name="form_info_1-structure"></a><span data-ttu-id="36dca-104">FORM_INFO_1 Struktur</span><span class="sxs-lookup"><span data-stu-id="36dca-104">FORM_INFO_1 structure</span></span>

<span data-ttu-id="36dca-105">Die **FORM_INFO_1** -Struktur enthält Informationen zu einem Druckformular.</span><span class="sxs-lookup"><span data-stu-id="36dca-105">The **FORM_INFO_1** structure contains information about a print form.</span></span> <span data-ttu-id="36dca-106">Die Informationen umfassen den Ursprung des Druck Formulars, den Namen, seine Dimensionen und die Abmessungen des druckbaren Bereichs.</span><span class="sxs-lookup"><span data-stu-id="36dca-106">The information includes the print form's origin, its name, its dimensions, and the dimensions of its printable area.</span></span>

## <a name="syntax"></a><span data-ttu-id="36dca-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="36dca-107">Syntax</span></span>


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a><span data-ttu-id="36dca-108">Member</span><span class="sxs-lookup"><span data-stu-id="36dca-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="36dca-109">**Flags**</span><span class="sxs-lookup"><span data-stu-id="36dca-109">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="36dca-110">Die Formular Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="36dca-110">The form properties.</span></span> <span data-ttu-id="36dca-111">Die folgenden Werte sind definiert.</span><span class="sxs-lookup"><span data-stu-id="36dca-111">The following values are defined.</span></span>



| <span data-ttu-id="36dca-112">Wert</span><span class="sxs-lookup"><span data-stu-id="36dca-112">Value</span></span>         | <span data-ttu-id="36dca-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="36dca-113">Meaning</span></span>                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36dca-114">FORM_USER</span><span class="sxs-lookup"><span data-stu-id="36dca-114">FORM_USER</span></span>    | <span data-ttu-id="36dca-115">Wenn dieses Bitflag festgelegt ist, wurde das Formular vom Benutzer definiert.</span><span class="sxs-lookup"><span data-stu-id="36dca-115">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="36dca-116">Formulare mit diesem Flagsatz werden in der Registrierung definiert.</span><span class="sxs-lookup"><span data-stu-id="36dca-116">Forms with this flag set are defined in the registry.</span></span>        |
| <span data-ttu-id="36dca-117">FORM_BUILTIN</span><span class="sxs-lookup"><span data-stu-id="36dca-117">FORM_BUILTIN</span></span> | <span data-ttu-id="36dca-118">Wenn dieses Bitflag festgelegt ist, ist das Formular Teil des Spoolers.</span><span class="sxs-lookup"><span data-stu-id="36dca-118">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="36dca-119">Formular Definitionen mit diesem Flagsatz werden nicht in der Registrierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="36dca-119">Form definitions with this flag set do not appear in the registry.</span></span> |
| <span data-ttu-id="36dca-120">FORM_PRINTER</span><span class="sxs-lookup"><span data-stu-id="36dca-120">FORM_PRINTER</span></span> | <span data-ttu-id="36dca-121">Wenn dieses Bitflag festgelegt ist, wird das Formular einem bestimmten Drucker zugeordnet, und seine Definition wird in der Registrierung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="36dca-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>          |



 

</dd> <dt>

<span data-ttu-id="36dca-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="36dca-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="36dca-123">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Formulars angibt.</span><span class="sxs-lookup"><span data-stu-id="36dca-123">Pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="36dca-124">Der Formular Name darf nicht länger als 31 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="36dca-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="36dca-125">**Größe**</span><span class="sxs-lookup"><span data-stu-id="36dca-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="36dca-126">Die Breite und Höhe des Formulars in tausendstel Millimeter.</span><span class="sxs-lookup"><span data-stu-id="36dca-126">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> <dt>

<span data-ttu-id="36dca-127">**Imageablearea**</span><span class="sxs-lookup"><span data-stu-id="36dca-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="36dca-128">Die Breite und Höhe des Formulars in tausendstel Millimeter.</span><span class="sxs-lookup"><span data-stu-id="36dca-128">The width and height, in thousandths of millimeters, of the form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36dca-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36dca-129">Requirements</span></span>



| <span data-ttu-id="36dca-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36dca-130">Requirement</span></span> | <span data-ttu-id="36dca-131">Wert</span><span class="sxs-lookup"><span data-stu-id="36dca-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36dca-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36dca-132">Minimum supported client</span></span><br/> | <span data-ttu-id="36dca-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36dca-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="36dca-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36dca-134">Minimum supported server</span></span><br/> | <span data-ttu-id="36dca-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36dca-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="36dca-136">Header</span><span class="sxs-lookup"><span data-stu-id="36dca-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="36dca-137"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36dca-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="36dca-138">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="36dca-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="36dca-139">**_FORM_INFO_1W** (Unicode) und **_FORM_INFO_1A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="36dca-139">**_FORM_INFO_1W** (Unicode) and **_FORM_INFO_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="36dca-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36dca-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36dca-141">Drucken</span><span class="sxs-lookup"><span data-stu-id="36dca-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="36dca-142">Druck Spooler-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="36dca-142">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="36dca-143">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="36dca-143">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="36dca-144">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="36dca-144">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="36dca-145">**Setform**</span><span class="sxs-lookup"><span data-stu-id="36dca-145">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




