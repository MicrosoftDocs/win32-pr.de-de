---
title: VS_VERSIONINFO Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Dabei handelt es sich um die Stamm Struktur, die alle anderen Datei Versions Informationsstrukturen enthält.
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- VS_VERSIONINFO Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106161"
---
# <a name="vs_versioninfo-structure"></a><span data-ttu-id="122fa-105">VS \_ VERSIONINFO-Struktur</span><span class="sxs-lookup"><span data-stu-id="122fa-105">VS\_VERSIONINFO structure</span></span>

<span data-ttu-id="122fa-106">Stellt die Organisation von Daten in einer Datei Versions Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="122fa-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="122fa-107">Dabei handelt es sich um die Stamm Struktur, die alle anderen Datei Versions Informationsstrukturen enthält.</span><span class="sxs-lookup"><span data-stu-id="122fa-107">It is the root structure that contains all other file-version information structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="122fa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="122fa-108">Syntax</span></span>


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="122fa-109">Member</span><span class="sxs-lookup"><span data-stu-id="122fa-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="122fa-110">**wlength**</span><span class="sxs-lookup"><span data-stu-id="122fa-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="122fa-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="122fa-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="122fa-112">Die Länge der **vs \_ VERSIONINFO** -Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="122fa-112">The length, in bytes, of the **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="122fa-113">Diese Länge schließt keine Auffüll Zeichen ein, die nachfolgende Versions Ressourcen Daten an einer 32-Bit-Grenze ausrichten.</span><span class="sxs-lookup"><span data-stu-id="122fa-113">This length does not include any padding that aligns any subsequent version resource data on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="122fa-114">**wvaluelength**</span><span class="sxs-lookup"><span data-stu-id="122fa-114">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="122fa-115">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="122fa-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="122fa-116">Die Länge (in Byte) des **Wertmembers** .</span><span class="sxs-lookup"><span data-stu-id="122fa-116">The length, in bytes, of the **Value** member.</span></span> <span data-ttu-id="122fa-117">Dieser Wert ist 0 (null), wenn der aktuellen Versions Struktur kein **Wert** Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="122fa-117">This value is zero if there is no **Value** member associated with the current version structure.</span></span>

</dd> <dt>

<span data-ttu-id="122fa-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="122fa-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="122fa-119">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="122fa-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="122fa-120">Der Typ der Daten in der Versions Ressource.</span><span class="sxs-lookup"><span data-stu-id="122fa-120">The type of data in the version resource.</span></span> <span data-ttu-id="122fa-121">Dieser Member ist 1, wenn die Versions Ressource Textdaten enthält, und 0, wenn die Versions Ressource binäre Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="122fa-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="122fa-122">**szkey**</span><span class="sxs-lookup"><span data-stu-id="122fa-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="122fa-123">Typ: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="122fa-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="122fa-124">Die Unicode-Zeichenfolge L "vs- \_ Versions \_ Informationen".</span><span class="sxs-lookup"><span data-stu-id="122fa-124">The Unicode string L"VS\_VERSION\_INFO".</span></span>

</dd> <dt>

<span data-ttu-id="122fa-125">**Padding1**</span><span class="sxs-lookup"><span data-stu-id="122fa-125">**Padding1**</span></span>
</dt> <dd>

<span data-ttu-id="122fa-126">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="122fa-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="122fa-127">Enthält so viele Null-Wörter, wie erforderlich, um den **Wertmember** an einer 32-Bit-Grenze auszurichten.</span><span class="sxs-lookup"><span data-stu-id="122fa-127">Contains as many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="122fa-128">**Wert**</span><span class="sxs-lookup"><span data-stu-id="122fa-128">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="122fa-129">Typ: **[ **vs \_ FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span><span class="sxs-lookup"><span data-stu-id="122fa-129">Type: **[**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span></span>

</dd> <dd>

<span data-ttu-id="122fa-130">Beliebige Daten, die dieser **vs \_ VERSIONINFO** -Struktur zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="122fa-130">Arbitrary data associated with this **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="122fa-131">Der **wvaluelength** -Member gibt die Länge dieses Members an. Wenn **wvaluelength** gleich 0 (null) ist, ist dieser Member nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="122fa-131">The **wValueLength** member specifies the length of this member; if **wValueLength** is zero, this member does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="122fa-132">**Padding2**</span><span class="sxs-lookup"><span data-stu-id="122fa-132">**Padding2**</span></span>
</dt> <dd>

<span data-ttu-id="122fa-133">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="122fa-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="122fa-134">So viele Null-Wörter, wie erforderlich, **um den unter** geordneten Member an einer 32-Bit-Grenze auszurichten.</span><span class="sxs-lookup"><span data-stu-id="122fa-134">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span> <span data-ttu-id="122fa-135">Diese Bytes sind nicht in **wvaluelength** enthalten.</span><span class="sxs-lookup"><span data-stu-id="122fa-135">These bytes are not included in **wValueLength**.</span></span> <span data-ttu-id="122fa-136">Dieses Member ist optional.</span><span class="sxs-lookup"><span data-stu-id="122fa-136">This member is optional.</span></span>

</dd> <dt>

<span data-ttu-id="122fa-137">**Children**</span><span class="sxs-lookup"><span data-stu-id="122fa-137">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="122fa-138">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="122fa-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="122fa-139">Ein Array von 0 (null) oder einer [**stringfileinfo**](stringfileinfo.md) -Struktur und NULL oder eine [**varfileinfo**](varfileinfo.md) -Struktur, die untergeordnete Elemente der aktuellen **vs \_ VERSIONINFO** -Struktur sind.</span><span class="sxs-lookup"><span data-stu-id="122fa-139">An array of zero or one [**StringFileInfo**](stringfileinfo.md) structures, and zero or one [**VarFileInfo**](varfileinfo.md) structures that are children of the current **VS\_VERSIONINFO** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="122fa-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="122fa-140">Remarks</span></span>

<span data-ttu-id="122fa-141">Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="122fa-141">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="122fa-142">Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="122fa-142">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="122fa-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="122fa-143">Requirements</span></span>



| <span data-ttu-id="122fa-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="122fa-144">Requirement</span></span> | <span data-ttu-id="122fa-145">Wert</span><span class="sxs-lookup"><span data-stu-id="122fa-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="122fa-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="122fa-146">Minimum supported client</span></span><br/> | <span data-ttu-id="122fa-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="122fa-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="122fa-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="122fa-148">Minimum supported server</span></span><br/> | <span data-ttu-id="122fa-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="122fa-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="122fa-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="122fa-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="122fa-151">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="122fa-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="122fa-152">**Stringfileingefo**</span><span class="sxs-lookup"><span data-stu-id="122fa-152">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="122fa-153">**VerQueryValue**</span><span class="sxs-lookup"><span data-stu-id="122fa-153">**VerQueryValue**</span></span>](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[<span data-ttu-id="122fa-154">**Varfileingefo**</span><span class="sxs-lookup"><span data-stu-id="122fa-154">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="122fa-155">**VS \_ fixedfileingefo**</span><span class="sxs-lookup"><span data-stu-id="122fa-155">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

<span data-ttu-id="122fa-156">**Licher**</span><span class="sxs-lookup"><span data-stu-id="122fa-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="122fa-157">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="122fa-157">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





