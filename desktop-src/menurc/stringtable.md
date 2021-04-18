---
title: STRINGTABLE-Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält sprach-und Code Page Formatierungsinformationen für die Zeichen folgen, die vom Children-Member angegeben werden. Eine Codepage ist ein geordneter Zeichensatz.
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- STRINGTABLE-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391653"
---
# <a name="stringtable-structure"></a><span data-ttu-id="e0dc2-106">STRINGTABLE-Struktur</span><span class="sxs-lookup"><span data-stu-id="e0dc2-106">StringTable structure</span></span>

<span data-ttu-id="e0dc2-107">Stellt die Organisation von Daten in einer Datei Versions Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-107">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="e0dc2-108">Sie enthält sprach-und Code Page Formatierungsinformationen für die Zeichen folgen, die vom **Children** -Member angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-108">It contains language and code page formatting information for the strings specified by the **Children** member.</span></span> <span data-ttu-id="e0dc2-109">Eine Codepage ist ein geordneter Zeichensatz.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-109">A code page is an ordered character set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0dc2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0dc2-110">Syntax</span></span>


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a><span data-ttu-id="e0dc2-111">Member</span><span class="sxs-lookup"><span data-stu-id="e0dc2-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0dc2-112">**wlength**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-112">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="e0dc2-113">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-113">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e0dc2-114">Die Länge der **STRINGTABLE** -Struktur in Bytes, einschließlich aller **vom untergeordneten** Element angegeben Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-114">The length, in bytes, of this **StringTable** structure, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="e0dc2-115">**wvaluelength**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-115">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="e0dc2-116">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e0dc2-117">Dieser Member ist immer gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e0dc2-117">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e0dc2-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="e0dc2-119">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e0dc2-120">Der Typ der Daten in der Versions Ressource.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-120">The type of data in the version resource.</span></span> <span data-ttu-id="e0dc2-121">Dieser Member ist 1, wenn die Versions Ressource Textdaten enthält, und 0, wenn die Versions Ressource binäre Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="e0dc2-122">**szkey**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="e0dc2-123">Typ: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="e0dc2-124">Eine 8-stellige hexadezimal Zahl, die als Unicode-Zeichenfolge gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-124">An 8-digit hexadecimal number stored as a Unicode string.</span></span> <span data-ttu-id="e0dc2-125">Die vier signifikantesten Ziffern stellen den sprach Bezeichner dar.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-125">The four most significant digits represent the language identifier.</span></span> <span data-ttu-id="e0dc2-126">Die vier wichtigsten Ziffern stellen die Codepage dar, für die die Daten formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-126">The four least significant digits represent the code page for which the data is formatted.</span></span> <span data-ttu-id="e0dc2-127">Jeder Bezeichner der Microsoft-Standard Sprache enthält zwei Teile: die nieder wertigen 10 Bits geben die Hauptsprache an, und die höherwertigen 6 Bits geben die unter Sprache an.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-127">Each Microsoft Standard Language identifier contains two parts: the low-order 10 bits specify the major language, and the high-order 6 bits specify the sublanguage.</span></span> <span data-ttu-id="e0dc2-128">Eine Tabelle gültiger Bezeichner finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-128">For a table of valid identifiers see .</span></span>

</dd> <dt>

<span data-ttu-id="e0dc2-129">**Auffüllen**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-129">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="e0dc2-130">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-130">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e0dc2-131">So viele Null-Wörter, wie erforderlich, **um den unter** geordneten Member an einer 32-Bit-Grenze auszurichten.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-131">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="e0dc2-132">**Children**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-132">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="e0dc2-133">Typ: **[ **Zeichenfolge**](string-str.md)**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-133">Type: **[**String**](string-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e0dc2-134">Ein Array aus einer oder mehreren [**Zeichen**](string-str.md) folgen Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-134">An array of one or more [**String**](string-str.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0dc2-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0dc2-135">Remarks</span></span>

<span data-ttu-id="e0dc2-136">Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-136">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="e0dc2-137">Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-137">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="e0dc2-138">Der **Children** -Member der [**stringfileinfo**](stringfileinfo.md) -Struktur enthält mindestens eine **STRINGTABLE** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-138">The **Children** member of the [**StringFileInfo**](stringfileinfo.md) structure contains at least one **StringTable** structure.</span></span>

<span data-ttu-id="e0dc2-139">Legen Sie den Codepage-Teil des **szkey** -Members auf den Hexadezimalwert 0x04b0 fest, um die Unicode-Codepage anzugeben, oder auf den Hexadezimalwert der Codepage, der für die Sprachkomponente geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-139">Set the code page portion of the **szKey** member to the hexadecimal value 0x04b0 to indicate the Unicode code page, or to the hexadecimal value of the code page that is appropriate for the language component.</span></span> <span data-ttu-id="e0dc2-140">Nachdem Sie den Wert für die Codepage ausgewählt haben, sollten Sie den gleichen Wert auch in späteren Revisionen der Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-140">After you choose the value for the code page you should continue to use the same value in later revisions to the file.</span></span>

<span data-ttu-id="e0dc2-141">Eine ausführbare Datei oder dll, die mehrere Sprachen unterstützt, sollte über eine Versions Ressource für jede Sprache verfügen, anstatt über eine einzige Versions Ressource, die Zeichen folgen in mehreren Sprachen enthält.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-141">An executable file or DLL that supports multiple languages should have a version resource for each language, rather than a single version resource that contains strings in several languages.</span></span> <span data-ttu-id="e0dc2-142">Wenn Sie jedoch die [**var**](var-str.md) -Struktur verwenden, um die Sprachen aufzulisten, die von der Anwendung unterstützt werden, ist die Anzahl der **STRINGTABLE** -Strukturen in der Versions Ressource direkt mit der Anzahl der sprach-/Codepage-bezeichnerpaare im **Wertmember** der **var** -Struktur verknüpft.</span><span class="sxs-lookup"><span data-stu-id="e0dc2-142">However, if you use the [**Var**](var-str.md) structure to list the languages that your application supports, the number of **StringTable** structures in the version resource is directly related to the number of language/code page identifier pairs in the **Value** member of the **Var** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0dc2-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0dc2-143">Requirements</span></span>



| <span data-ttu-id="e0dc2-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0dc2-144">Requirement</span></span> | <span data-ttu-id="e0dc2-145">Wert</span><span class="sxs-lookup"><span data-stu-id="e0dc2-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e0dc2-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0dc2-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e0dc2-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0dc2-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e0dc2-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0dc2-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e0dc2-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0dc2-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e0dc2-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0dc2-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="e0dc2-151">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e0dc2-152">**Schnür**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-152">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="e0dc2-153">**Stringfileingefo**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-153">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="e0dc2-154">**Kreis**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-154">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="e0dc2-155">**Varfileingefo**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-155">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="e0dc2-156">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-156">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="e0dc2-157">**Licher**</span><span class="sxs-lookup"><span data-stu-id="e0dc2-157">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e0dc2-158">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="e0dc2-158">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





