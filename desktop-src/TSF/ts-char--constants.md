---
title: TS_CHAR_ Konstanten (textstor. h)
description: Die TS \_ Char \_ \-Konstanten beschreiben den Typ des Zeichens.
ms.assetid: b40ca931-d45c-4101-9380-bb2b3ad25fba
topic_type:
- apiref
api_name:
- TS_CHAR_EMBEDDED
- TS_CHAR_REGION
- TS_CHAR_REPLACEMENT
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25f66006dcb37e2504785b2b28ca1f328edfcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391768"
---
# <a name="ts_char_-constants"></a><span data-ttu-id="421f8-103">TS \_ Char- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="421f8-103">TS\_CHAR\_\* Constants</span></span>

<span data-ttu-id="421f8-104">Die TS- \_ Char- \_ \* Konstanten beschreiben den Typ des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="421f8-104">The TS\_CHAR\_\* constants describe the type of character.</span></span>



| <span data-ttu-id="421f8-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="421f8-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="421f8-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="421f8-106">Description</span></span>                                                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| <span id="TS_CHAR_EMBEDDED"></span><span id="ts_char_embedded"></span><dl> <span data-ttu-id="421f8-107"><dt>**TS \_ Char \_ Embedded**</dt> <dt>(0xfffc)</dt></span><span class="sxs-lookup"><span data-stu-id="421f8-107"><dt>**TS\_CHAR\_EMBEDDED**</dt> <dt>( 0xfffc )</dt></span></span> </dl>          | <span data-ttu-id="421f8-108">Das Zeichen ist ein Unicode 2,1-Objekt Austausch Zeichen.</span><span class="sxs-lookup"><span data-stu-id="421f8-108">The character is a Unicode 2.1 object-replacement character.</span></span><br/>                             |
| <span id="TS_CHAR_REGION"></span><span id="ts_char_region"></span><dl> <span data-ttu-id="421f8-109"><dt>**TS \_ Char- \_ Region**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="421f8-109"><dt>**TS\_CHAR\_REGION**</dt> <dt>( 0 )</dt></span></span> </dl>                     | <span data-ttu-id="421f8-110">Das Zeichen ist eine Regions Grenze.</span><span class="sxs-lookup"><span data-stu-id="421f8-110">The character is a region boundary.</span></span><br/>                                                      |
| <span id="TS_CHAR_REPLACEMENT"></span><span id="ts_char_replacement"></span><dl> <span data-ttu-id="421f8-111"><dt>**TS \_ Char- \_ Ersetzung**</dt> <dt>(0xFFFD)</dt></span><span class="sxs-lookup"><span data-stu-id="421f8-111"><dt>**TS\_CHAR\_REPLACEMENT**</dt> <dt>( 0xfffd )</dt></span></span> </dl> | <span data-ttu-id="421f8-112">Das Zeichen ist ein Platzhalter Zeichen oder ein Unicode-Ersatz Zeichen.</span><span class="sxs-lookup"><span data-stu-id="421f8-112">The character is a hidden-text placeholder character or a Unicode replacement character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="421f8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="421f8-113">Requirements</span></span>



| <span data-ttu-id="421f8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="421f8-114">Requirement</span></span> | <span data-ttu-id="421f8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="421f8-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="421f8-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="421f8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="421f8-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="421f8-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="421f8-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="421f8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="421f8-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="421f8-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="421f8-120">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="421f8-120">Redistributable</span></span><br/>          | <span data-ttu-id="421f8-121">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="421f8-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="421f8-122">Header</span><span class="sxs-lookup"><span data-stu-id="421f8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="421f8-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="421f8-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="421f8-124">IDL</span><span class="sxs-lookup"><span data-stu-id="421f8-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="421f8-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="421f8-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="421f8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="421f8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="421f8-127">Eingebettete Objekte</span><span class="sxs-lookup"><span data-stu-id="421f8-127">Embedded Objects</span></span>](embedded-objects.md)
</dt> </dl>

 

 





