---
title: Stringfileingefo-Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält Versionsinformationen, die für eine bestimmte Sprache und Codepage angezeigt werden können.
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- Stringfileingefo-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949551"
---
# <a name="stringfileinfo-structure"></a><span data-ttu-id="eaa15-105">Stringfileingefo-Struktur</span><span class="sxs-lookup"><span data-stu-id="eaa15-105">StringFileInfo structure</span></span>

<span data-ttu-id="eaa15-106">Stellt die Organisation von Daten in einer Datei Versions Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="eaa15-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="eaa15-107">Sie enthält Versionsinformationen, die für eine bestimmte Sprache und Codepage angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="eaa15-107">It contains version information that can be displayed for a particular language and code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaa15-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaa15-108">Syntax</span></span>


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a><span data-ttu-id="eaa15-109">Member</span><span class="sxs-lookup"><span data-stu-id="eaa15-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="eaa15-110">**wlength**</span><span class="sxs-lookup"><span data-stu-id="eaa15-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="eaa15-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="eaa15-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="eaa15-112">Die Länge des gesamten **stringfileinfo** -Blocks in Bytes, einschließlich aller **vom untergeordneten** Element angegeben Strukturen.</span><span class="sxs-lookup"><span data-stu-id="eaa15-112">The length, in bytes, of the entire **StringFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="eaa15-113">**wvaluelength**</span><span class="sxs-lookup"><span data-stu-id="eaa15-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="eaa15-114">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="eaa15-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="eaa15-115">Dieser Member ist immer gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="eaa15-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="eaa15-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="eaa15-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="eaa15-117">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="eaa15-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="eaa15-118">Der Typ der Daten in der Versions Ressource.</span><span class="sxs-lookup"><span data-stu-id="eaa15-118">The type of data in the version resource.</span></span> <span data-ttu-id="eaa15-119">Dieser Member ist 1, wenn die Versions Ressource Textdaten enthält, und 0, wenn die Versions Ressource binäre Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="eaa15-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="eaa15-120">**szkey**</span><span class="sxs-lookup"><span data-stu-id="eaa15-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="eaa15-121">Typ: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="eaa15-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="eaa15-122">Die Unicode-Zeichenfolge L "stringfileingefo".</span><span class="sxs-lookup"><span data-stu-id="eaa15-122">The Unicode string L"StringFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="eaa15-123">**Auffüllen**</span><span class="sxs-lookup"><span data-stu-id="eaa15-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="eaa15-124">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="eaa15-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="eaa15-125">So viele Null-Wörter, wie erforderlich, **um den unter** geordneten Member an einer 32-Bit-Grenze auszurichten.</span><span class="sxs-lookup"><span data-stu-id="eaa15-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="eaa15-126">**Children**</span><span class="sxs-lookup"><span data-stu-id="eaa15-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="eaa15-127">Typ: **[ **STRINGTABLE**](stringtable.md)**</span><span class="sxs-lookup"><span data-stu-id="eaa15-127">Type: **[**StringTable**](stringtable.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eaa15-128">Ein Array mit einem oder mehreren [**STRINGTABLE**](stringtable.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="eaa15-128">An array of one or more [**StringTable**](stringtable.md) structures.</span></span> <span data-ttu-id="eaa15-129">Jeder **szkey** -Member der **STRINGTABLE** -Struktur gibt die entsprechende Sprache und Codepage zum Anzeigen des Texts in der **STRINGTABLE** -Struktur an.</span><span class="sxs-lookup"><span data-stu-id="eaa15-129">Each **StringTable** structure's **szKey** member indicates the appropriate language and code page for displaying the text in that **StringTable** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eaa15-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaa15-130">Remarks</span></span>

<span data-ttu-id="eaa15-131">Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="eaa15-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="eaa15-132">Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="eaa15-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="eaa15-133">Das **Children** -Element der [**vs \_ VERSIONINFO**](vs-versioninfo.md) -Struktur kann NULL oder mehr **stringfileinfo** -Strukturen enthalten.</span><span class="sxs-lookup"><span data-stu-id="eaa15-133">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or more **StringFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa15-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaa15-134">Requirements</span></span>



| <span data-ttu-id="eaa15-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaa15-135">Requirement</span></span> | <span data-ttu-id="eaa15-136">Wert</span><span class="sxs-lookup"><span data-stu-id="eaa15-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="eaa15-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eaa15-137">Minimum supported client</span></span><br/> | <span data-ttu-id="eaa15-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaa15-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="eaa15-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eaa15-139">Minimum supported server</span></span><br/> | <span data-ttu-id="eaa15-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaa15-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="eaa15-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eaa15-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="eaa15-142">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="eaa15-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eaa15-143">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="eaa15-143">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="eaa15-144">**Schnür**</span><span class="sxs-lookup"><span data-stu-id="eaa15-144">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="eaa15-145">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="eaa15-145">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="eaa15-146">**Licher**</span><span class="sxs-lookup"><span data-stu-id="eaa15-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eaa15-147">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="eaa15-147">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





