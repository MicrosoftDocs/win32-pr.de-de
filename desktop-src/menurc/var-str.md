---
title: Var-Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält in der Regel eine Liste der Sprachen-und Codepage-bezeichnerpaare, die von der Version der Anwendung oder DLL unterstützt werden.
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Var Structure-Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859257"
---
# <a name="var-structure"></a><span data-ttu-id="a6dbe-105">Var-Struktur</span><span class="sxs-lookup"><span data-stu-id="a6dbe-105">Var structure</span></span>

<span data-ttu-id="a6dbe-106">Stellt die Organisation von Daten in einer Datei Versions Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="a6dbe-107">Sie enthält in der Regel eine Liste der Sprachen-und Codepage-bezeichnerpaare, die von der Version der Anwendung oder DLL unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-107">It typically contains a list of language and code page identifier pairs that the version of the application or DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6dbe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6dbe-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a><span data-ttu-id="a6dbe-109">Member</span><span class="sxs-lookup"><span data-stu-id="a6dbe-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="a6dbe-110">**wlength**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="a6dbe-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="a6dbe-112">Die Länge der **var** -Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-112">The length, in bytes, of the **Var** structure.</span></span>

</dd> <dt>

<span data-ttu-id="a6dbe-113">**wvaluelength**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="a6dbe-114">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="a6dbe-115">Die Länge (in Byte) des **Wertmembers** .</span><span class="sxs-lookup"><span data-stu-id="a6dbe-115">The length, in bytes, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="a6dbe-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="a6dbe-117">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="a6dbe-118">Der Typ der Daten in der Versions Ressource.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-118">The type of data in the version resource.</span></span> <span data-ttu-id="a6dbe-119">Dieser Member ist 1, wenn die Versions Ressource Textdaten enthält, und 0, wenn die Versions Ressource binäre Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="a6dbe-120">**szkey**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="a6dbe-121">Typ: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="a6dbe-122">Die Unicode-Zeichenfolge L "Translation".</span><span class="sxs-lookup"><span data-stu-id="a6dbe-122">The Unicode string L"Translation".</span></span>

</dd> <dt>

<span data-ttu-id="a6dbe-123">**Auffüllen**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="a6dbe-124">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="a6dbe-125">So viele Null-Wörter, wie erforderlich, um den **Wertmember** an einer 32-Bit-Grenze auszurichten.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-125">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="a6dbe-126">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-126">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="a6dbe-127">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="a6dbe-128">Ein Array von einem oder mehreren Werten, die Sprach-und Codepage-bezeichnerpaare sind.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-128">An array of one or more values that are language and code page identifier pairs.</span></span> <span data-ttu-id="a6dbe-129">Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="a6dbe-129">For additional information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6dbe-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6dbe-130">Remarks</span></span>

<span data-ttu-id="a6dbe-131">Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="a6dbe-132">Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="a6dbe-133">Wenn Sie die **var** -Struktur verwenden, um die Sprachen aufzulisten, die Ihre Anwendung oder DLL unterstützt, anstatt mehrere Versions Ressourcen zu verwenden, verwenden Sie das **Wertmember** , um ein Array von **DWORD** -Werten anzugeben, die die von dieser Datei unterstützten Kombinationen von Sprache und Codepage angeben</span><span class="sxs-lookup"><span data-stu-id="a6dbe-133">If you use the **Var** structure to list the languages your application or DLL supports instead of using multiple version resources, use the **Value** member to contain an array of **DWORD** values indicating the language and code page combinations supported by this file.</span></span> <span data-ttu-id="a6dbe-134">Das nieder wertige Wort jedes **DWORD** muss einen Microsoft-Sprachen Bezeichner enthalten, und das höchst wertige Wort muss die IBM-Code Page Nummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-134">The low-order word of each **DWORD** must contain a Microsoft language identifier, and the high-order word must contain the IBM code page number.</span></span> <span data-ttu-id="a6dbe-135">Ein Wort mit hoher Reihenfolge oder niedriger Ordnung kann NULL sein, was darauf hinweist, dass die Datei sprach-oder Codepage-unabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-135">Either high-order or low-order word can be zero, indicating that the file is language or code page independent.</span></span> <span data-ttu-id="a6dbe-136">Wenn die **var** -Struktur weggelassen wird, wird die Datei als Sprache und Codepage unabhängig interpretiert.</span><span class="sxs-lookup"><span data-stu-id="a6dbe-136">If the **Var** structure is omitted, the file will be interpreted as both language and code page independent.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6dbe-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6dbe-137">Requirements</span></span>



| <span data-ttu-id="a6dbe-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6dbe-138">Requirement</span></span> | <span data-ttu-id="a6dbe-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a6dbe-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a6dbe-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6dbe-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a6dbe-141">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6dbe-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a6dbe-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6dbe-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a6dbe-143">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6dbe-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a6dbe-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6dbe-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6dbe-145">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a6dbe-146">**Varfileingefo**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-146">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="a6dbe-147">**Stringfileingefo**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-147">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="a6dbe-148">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-148">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="a6dbe-149">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-149">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="a6dbe-150">**Licher**</span><span class="sxs-lookup"><span data-stu-id="a6dbe-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a6dbe-151">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="a6dbe-151">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





