---
title: TS_IAS_ Konstanten (textstor. h)
description: Die TS \_ IAS \_ \-Konstanten werden als bitfeldflags verwendet, um das Einfügen von Text oder eingebetteten Objekten an einer Auswahl-oder Einfügemarke zu steuern.
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103815"
---
# <a name="ts_ias_-constants"></a><span data-ttu-id="53bce-103">TS \_ IAS- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="53bce-103">TS\_IAS\_\* Constants</span></span>

<span data-ttu-id="53bce-104">Die TS \_ IAS- \_ \* Konstanten werden als bitfeldflags verwendet, um das Einfügen von Text oder eingebetteten Objekten an einer Auswahl-oder Einfügemarke zu steuern.</span><span class="sxs-lookup"><span data-stu-id="53bce-104">The TS\_IAS\_\* constants are used as bitfield flags to control insertion of text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="53bce-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="53bce-105">Constant/value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="53bce-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53bce-106">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <span data-ttu-id="53bce-107"><dt>**TS \_ IAS \_ noquery**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="53bce-107"><dt>**TS\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>       | <span data-ttu-id="53bce-108">Der Text wird eingefügt, und der Bereichs Zeiger wird beim Beenden auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="53bce-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="53bce-109">Kann nicht mit dem TS \_ IAS- \_ Flag queryonly kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="53bce-109">Cannot be combined with the TS\_IAS\_QUERYONLY flag.</span></span><br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <span data-ttu-id="53bce-110"><dt>**TS \_ IAS- \_ queryonly**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="53bce-110"><dt>**TS\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="53bce-111">Führen Sie die Einfügung nicht aus.</span><span class="sxs-lookup"><span data-stu-id="53bce-111">Do not perform the insertion.</span></span> <span data-ttu-id="53bce-112">Für den Aufrufer muss nur der Bereichs Zeiger festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="53bce-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="53bce-113">Kann nicht mit dem TS \_ IAS \_ noquery-Flag kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="53bce-113">Cannot be combined with the TS\_IAS\_NOQUERY flag.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="53bce-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53bce-114">Requirements</span></span>



| <span data-ttu-id="53bce-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53bce-115">Requirement</span></span> | <span data-ttu-id="53bce-116">Wert</span><span class="sxs-lookup"><span data-stu-id="53bce-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53bce-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53bce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53bce-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53bce-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="53bce-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53bce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53bce-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53bce-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="53bce-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="53bce-121">Redistributable</span></span><br/>          | <span data-ttu-id="53bce-122">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="53bce-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="53bce-123">Header</span><span class="sxs-lookup"><span data-stu-id="53bce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="53bce-124"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="53bce-124"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="53bce-125">IDL</span><span class="sxs-lookup"><span data-stu-id="53bce-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="53bce-126"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="53bce-126"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





