---
title: Fontgrouphdr-Struktur
description: Enthält die Informationen, die für eine Anwendung erforderlich sind, um auf eine bestimmte Schriftart zuzugreifen. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- Fontgrouphdr-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d67d9ecfa451970422f21d05817f26170a9c8eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213734"
---
# <a name="fontgrouphdr-structure"></a><span data-ttu-id="262a0-105">Fontgrouphdr-Struktur</span><span class="sxs-lookup"><span data-stu-id="262a0-105">FONTGROUPHDR structure</span></span>

<span data-ttu-id="262a0-106">Enthält die Informationen, die für eine Anwendung erforderlich sind, um auf eine bestimmte Schriftart zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="262a0-106">Contains the information necessary for an application to access a specific font.</span></span> <span data-ttu-id="262a0-107">Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="262a0-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="262a0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="262a0-108">Syntax</span></span>


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a><span data-ttu-id="262a0-109">Member</span><span class="sxs-lookup"><span data-stu-id="262a0-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="262a0-110">**Numoffonts**</span><span class="sxs-lookup"><span data-stu-id="262a0-110">**NumberOfFonts**</span></span>
</dt> <dd>

<span data-ttu-id="262a0-111">Typ: **Word**</span><span class="sxs-lookup"><span data-stu-id="262a0-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="262a0-112">Die Anzahl der einzelnen Schriftarten, die dieser Ressource zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="262a0-112">The number of individual fonts associated with this resource.</span></span>

</dd> <dt>

<span data-ttu-id="262a0-113">**DE**</span><span class="sxs-lookup"><span data-stu-id="262a0-113">**DE**</span></span>
</dt> <dd>

<span data-ttu-id="262a0-114">Typ: **[ **direntry**](direntry.md)**</span><span class="sxs-lookup"><span data-stu-id="262a0-114">Type: **[**DIRENTRY**](direntry.md)**</span></span>

</dd> <dd>

<span data-ttu-id="262a0-115">Eine-Struktur, die einen eindeutigen ordinalbezeichner für jede Schriftart in der Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="262a0-115">A structure that contains a unique ordinal identifier for each font in the resource.</span></span> <span data-ttu-id="262a0-116">Der Member " **de** " ist ein Platzhalter für das Array mit [**direntry**](direntry.md) -Strukturen variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="262a0-116">The **DE** member is a placeholder for the variable-length array of [**DIRENTRY**](direntry.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="262a0-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="262a0-117">Remarks</span></span>

<span data-ttu-id="262a0-118">Die **fontgrouphdr** -Struktur folgt den Daten für die einzelnen Schriftarten in. Res-Datei.</span><span class="sxs-lookup"><span data-stu-id="262a0-118">The **FONTGROUPHDR** structure follows the data for the individual fonts in the .Res file.</span></span> <span data-ttu-id="262a0-119">Der Ressourcen Compiler fügt die **fontgrouphdr** -Struktur in der Regel automatisch als letzten Eintrag in der Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="262a0-119">The resource compiler automatically adds the **FONTGROUPHDR** structure, generally as the last entry in the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="262a0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="262a0-120">Requirements</span></span>



| <span data-ttu-id="262a0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="262a0-121">Requirement</span></span> | <span data-ttu-id="262a0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="262a0-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="262a0-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="262a0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="262a0-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="262a0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="262a0-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="262a0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="262a0-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="262a0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="262a0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="262a0-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="262a0-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="262a0-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="262a0-129">**Direntry**</span><span class="sxs-lookup"><span data-stu-id="262a0-129">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="262a0-130">**Fontdirentry**</span><span class="sxs-lookup"><span data-stu-id="262a0-130">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

<span data-ttu-id="262a0-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="262a0-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="262a0-132">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="262a0-132">Resources</span></span>](resources.md)
</dt> </dl>

 

 





