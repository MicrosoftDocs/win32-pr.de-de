---
description: Enthält die Attributdaten für eine Datei.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: Attrinfo-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860614"
---
# <a name="attrinfo-structure"></a><span data-ttu-id="76aaa-103">Attrinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="76aaa-103">ATTRINFO structure</span></span>

<span data-ttu-id="76aaa-104">Enthält die Attributdaten für eine Datei.</span><span class="sxs-lookup"><span data-stu-id="76aaa-104">Contains the attribute data for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="76aaa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76aaa-105">Syntax</span></span>


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a><span data-ttu-id="76aaa-106">Member</span><span class="sxs-lookup"><span data-stu-id="76aaa-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="76aaa-107">**tattrierer**</span><span class="sxs-lookup"><span data-stu-id="76aaa-107">**tAttrID**</span></span>
</dt> <dd>

<span data-ttu-id="76aaa-108">Der Attributtyp.</span><span class="sxs-lookup"><span data-stu-id="76aaa-108">The attribute type.</span></span> <span data-ttu-id="76aaa-109">Siehe [Tagtypen](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="76aaa-109">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="76aaa-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="76aaa-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="76aaa-111">Die Flags für dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="76aaa-111">The flags for this attribute.</span></span>



| <span data-ttu-id="76aaa-112">Wert</span><span class="sxs-lookup"><span data-stu-id="76aaa-112">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="76aaa-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="76aaa-113">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <span data-ttu-id="76aaa-114"><dt>**Attribut \_ Verfügbare**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="76aaa-114"><dt>**ATTRIBUTE\_AVAILABLE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="76aaa-115">Das-Attribut ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76aaa-115">The attribute is available.</span></span><br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <span data-ttu-id="76aaa-116"><dt>**Attribut \_**</dt>Fehler bei <dt>0x00000002</dt> .</span><span class="sxs-lookup"><span data-stu-id="76aaa-116"><dt>**ATTRIBUTE\_FAILED**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="76aaa-117">Der-Rückruf ist fehlgeschlagen, da das-Attribut nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="76aaa-117">The call failed because the attribute is not available.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="76aaa-118">**ullattr**</span><span class="sxs-lookup"><span data-stu-id="76aaa-118">**ullAttr**</span></span>
</dt> <dd>

<span data-ttu-id="76aaa-119">Ein **QWORD** -Wert (wenn der Tagtyp **\_ \_ QWORD** ist).</span><span class="sxs-lookup"><span data-stu-id="76aaa-119">A **QWORD** value (if the tag type is **TAG\_TYPE\_QWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="76aaa-120">**dwattr**</span><span class="sxs-lookup"><span data-stu-id="76aaa-120">**dwAttr**</span></span>
</dt> <dd>

<span data-ttu-id="76aaa-121">Ein **DWORD** -Wert (wenn der Tagtyp **\_ \_ DWORD** ist).</span><span class="sxs-lookup"><span data-stu-id="76aaa-121">A **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="76aaa-122">**lpattr**</span><span class="sxs-lookup"><span data-stu-id="76aaa-122">**lpAttr**</span></span>
</dt> <dd>

<span data-ttu-id="76aaa-123">Ein Zeiger auf eine Zeichenfolge (wenn der Tagtyp **" \_ TagType \_**" ist).</span><span class="sxs-lookup"><span data-stu-id="76aaa-123">A pointer to a string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76aaa-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76aaa-124">Requirements</span></span>



| <span data-ttu-id="76aaa-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76aaa-125">Requirement</span></span> | <span data-ttu-id="76aaa-126">Wert</span><span class="sxs-lookup"><span data-stu-id="76aaa-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="76aaa-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76aaa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="76aaa-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76aaa-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="76aaa-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76aaa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="76aaa-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76aaa-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="76aaa-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76aaa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76aaa-132">**Sdbformatattribute**</span><span class="sxs-lookup"><span data-stu-id="76aaa-132">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="76aaa-133">**Sdbfrefileattribute**</span><span class="sxs-lookup"><span data-stu-id="76aaa-133">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> <dt>

[<span data-ttu-id="76aaa-134">**Sdbgetfileattribute**</span><span class="sxs-lookup"><span data-stu-id="76aaa-134">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




