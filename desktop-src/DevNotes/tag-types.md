---
description: Beschreibt den Datentyp des Werts, der einem Tag zugeordnet ist.
ms.assetid: 009ad522-35da-4053-a7f6-61d7d240b98c
title: Tagtypen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab53b9c3b85263ddcdbe80e3979d576685bd73
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214067"
---
# <a name="tag-types"></a><span data-ttu-id="3ff8b-103">Tagtypen</span><span class="sxs-lookup"><span data-stu-id="3ff8b-103">TAG Types</span></span>

<span data-ttu-id="3ff8b-104">Beschreibt den Datentyp des Werts, der einem Tag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-104">Describes the data type of the value associated with a TAG.</span></span>



| <span data-ttu-id="3ff8b-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="3ff8b-105">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="3ff8b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ff8b-106">Description</span></span>                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span id="TAG_TYPE_NULL"></span><span id="tag_type_null"></span><dl> <span data-ttu-id="3ff8b-107"><dt>**Tag \_ Geben Sie \_ null**</dt> <dt>0x1000</dt> ein.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-107"><dt>**TAG\_TYPE\_NULL**</dt> <dt>0x1000</dt></span></span> </dl>                | <span data-ttu-id="3ff8b-108">Dem Tag ist kein Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-108">There is no value associated with the TAG.</span></span><br/> |
| <span id="TAG_TYPE_BYTE"></span><span id="tag_type_byte"></span><dl> <span data-ttu-id="3ff8b-109"><dt>**Tag \_ \_Typbyte**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff8b-109"><dt>**TAG\_TYPE\_BYTE**</dt> <dt>0x2000</dt></span></span> </dl>                | <span data-ttu-id="3ff8b-110">Ein **Bytewert** .</span><span class="sxs-lookup"><span data-stu-id="3ff8b-110">A **BYTE** value.</span></span><br/>                          |
| <span id="TAG_TYPE_WORD"></span><span id="tag_type_word"></span><dl> <span data-ttu-id="3ff8b-111"><dt>**Tag \_ Geben Sie \_ Word**</dt> <dt>0x3000</dt> ein.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-111"><dt>**TAG\_TYPE\_WORD**</dt> <dt>0x3000</dt></span></span> </dl>                | <span data-ttu-id="3ff8b-112">Ein **Wort** Wert.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-112">A **WORD** value.</span></span><br/>                          |
| <span id="TAG_TYPE_DWORD"></span><span id="tag_type_dword"></span><dl> <span data-ttu-id="3ff8b-113"><dt>**Tag \_ Typ \_ DWORD**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff8b-113"><dt>**TAG\_TYPE\_DWORD**</dt> <dt>0x4000</dt></span></span> </dl>             | <span data-ttu-id="3ff8b-114">Ein **DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-114">A **DWORD** value.</span></span><br/>                         |
| <span id="TAG_TYPE_QWORD"></span><span id="tag_type_qword"></span><dl> <span data-ttu-id="3ff8b-115"><dt>**Tag \_ Geben Sie \_ QWORD**</dt> <dt>0x5.000</dt> ein.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-115"><dt>**TAG\_TYPE\_QWORD**</dt> <dt>0x5000</dt></span></span> </dl>             | <span data-ttu-id="3ff8b-116">Ein **ULONGLONG** -Wert.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-116">A **ULONGLONG** value.</span></span><br/>                     |
| <span id="TAG_TYPE_STRINGREF"></span><span id="tag_type_stringref"></span><dl> <span data-ttu-id="3ff8b-117"><dt>**Tag \_ Geben Sie " \_ strauf**</dt> <dt>0x6000</dt> " ein.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-117"><dt>**TAG\_TYPE\_STRINGREF**</dt> <dt>0x6000</dt></span></span> </dl> | <span data-ttu-id="3ff8b-118">Ein tokenzeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-118">A tokenized string value.</span></span><br/>                  |
| <span id="TAG_TYPE_LIST"></span><span id="tag_type_list"></span><dl> <span data-ttu-id="3ff8b-119"><dt>**Tag \_ \_Typliste**</dt> <dt>0x7000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff8b-119"><dt>**TAG\_TYPE\_LIST**</dt> <dt>0x7000</dt></span></span> </dl>                | <span data-ttu-id="3ff8b-120">Eine Liste mit Tagwerten.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-120">A list of TAG values.</span></span><br/>                      |
| <span id="TAG_TYPE_STRING"></span><span id="tag_type_string"></span><dl> <span data-ttu-id="3ff8b-121"><dt>**Tag \_ \_Typzeichenfolge**</dt> <dt>0X8000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff8b-121"><dt>**TAG\_TYPE\_STRING**</dt> <dt>0x8000</dt></span></span> </dl>          | <span data-ttu-id="3ff8b-122">Ein Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-122">A string value.</span></span><br/>                            |
| <span id="TAG_TYPE_BINARY"></span><span id="tag_type_binary"></span><dl> <span data-ttu-id="3ff8b-123"><dt>**Tag \_ \_Typbinär Datei**</dt> <dt>0x9000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff8b-123"><dt>**TAG\_TYPE\_BINARY**</dt> <dt>0x9000</dt></span></span> </dl>          | <span data-ttu-id="3ff8b-124">Ein Binärwert.</span><span class="sxs-lookup"><span data-stu-id="3ff8b-124">A binary value.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="3ff8b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ff8b-125">Requirements</span></span>



| <span data-ttu-id="3ff8b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ff8b-126">Requirement</span></span> | <span data-ttu-id="3ff8b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="3ff8b-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ff8b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ff8b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3ff8b-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ff8b-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3ff8b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ff8b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3ff8b-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ff8b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ff8b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ff8b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ff8b-133">**Tag**</span><span class="sxs-lookup"><span data-stu-id="3ff8b-133">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="3ff8b-134">**TagID**</span><span class="sxs-lookup"><span data-stu-id="3ff8b-134">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="3ff8b-135">**Tagref**</span><span class="sxs-lookup"><span data-stu-id="3ff8b-135">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




