---
title: Varfileingefo-Struktur
description: Stellt die Organisation von Daten in einer Datei Versions Ressource dar. Sie enthält Versionsinformationen, die nicht von einer bestimmten Sprache und Codepage kombiniert werden.
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- Varfileingefo-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344090"
---
# <a name="varfileinfo-structure"></a><span data-ttu-id="06292-105">Varfileingefo-Struktur</span><span class="sxs-lookup"><span data-stu-id="06292-105">VarFileInfo structure</span></span>

<span data-ttu-id="06292-106">Stellt die Organisation von Daten in einer Datei Versions Ressource dar.</span><span class="sxs-lookup"><span data-stu-id="06292-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="06292-107">Sie enthält Versionsinformationen, die nicht von einer bestimmten Sprache und Codepage kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="06292-107">It contains version information not dependent on a particular language and code page combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="06292-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="06292-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a><span data-ttu-id="06292-109">Member</span><span class="sxs-lookup"><span data-stu-id="06292-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="06292-110">**wlength**</span><span class="sxs-lookup"><span data-stu-id="06292-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="06292-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="06292-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="06292-112">Die Länge des gesamten **varfileinfo** -Blocks (in Bytes), einschließlich aller Strukturen, die vom **Children** -Member angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="06292-112">The length, in bytes, of the entire **VarFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="06292-113">**wvaluelength**</span><span class="sxs-lookup"><span data-stu-id="06292-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="06292-114">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="06292-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="06292-115">Dieser Member ist immer gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="06292-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="06292-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="06292-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="06292-117">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="06292-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="06292-118">Der Typ der Daten in der Versions Ressource.</span><span class="sxs-lookup"><span data-stu-id="06292-118">The type of data in the version resource.</span></span> <span data-ttu-id="06292-119">Dieser Member ist 1, wenn die Versions Ressource Textdaten enthält, und 0, wenn die Versions Ressource binäre Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="06292-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="06292-120">**szkey**</span><span class="sxs-lookup"><span data-stu-id="06292-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="06292-121">Typ: **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="06292-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="06292-122">Die Unicode-Zeichenfolge L "varfileingefo".</span><span class="sxs-lookup"><span data-stu-id="06292-122">The Unicode string L"VarFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="06292-123">**Auffüllen**</span><span class="sxs-lookup"><span data-stu-id="06292-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="06292-124">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="06292-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="06292-125">So viele Null-Wörter, wie erforderlich, **um den unter** geordneten Member an einer 32-Bit-Grenze auszurichten.</span><span class="sxs-lookup"><span data-stu-id="06292-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="06292-126">**Children**</span><span class="sxs-lookup"><span data-stu-id="06292-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="06292-127">Typ: **[ **var**](var-str.md)**</span><span class="sxs-lookup"><span data-stu-id="06292-127">Type: **[**Var**](var-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="06292-128">Enthält in der Regel eine Liste der Sprachen, die von der Anwendung oder DLL unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="06292-128">Typically contains a list of languages that the application or DLL supports.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06292-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06292-129">Remarks</span></span>

<span data-ttu-id="06292-130">Diese Struktur ist keine echte C-Sprachstruktur, da Sie Member variabler Länge enthält.</span><span class="sxs-lookup"><span data-stu-id="06292-130">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="06292-131">Diese Struktur wurde ausschließlich zur Darstellung der Organisation von Daten in einer Versions Ressource erstellt und wird nicht in den Header Dateien angezeigt, die im Windows Software Development Kit (SDK) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="06292-131">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="06292-132">Das **unter** geordnete Element der [**vs \_ VERSIONINFO**](vs-versioninfo.md) -Struktur kann NULL oder eine **varfileinfo** -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="06292-132">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or one **VarFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="06292-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06292-133">Requirements</span></span>



| <span data-ttu-id="06292-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06292-134">Requirement</span></span> | <span data-ttu-id="06292-135">Wert</span><span class="sxs-lookup"><span data-stu-id="06292-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="06292-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06292-136">Minimum supported client</span></span><br/> | <span data-ttu-id="06292-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06292-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="06292-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06292-138">Minimum supported server</span></span><br/> | <span data-ttu-id="06292-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06292-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="06292-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06292-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="06292-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="06292-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="06292-142">**Kreis**</span><span class="sxs-lookup"><span data-stu-id="06292-142">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="06292-143">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="06292-143">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="06292-144">**Licher**</span><span class="sxs-lookup"><span data-stu-id="06292-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="06292-145">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="06292-145">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





