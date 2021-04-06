---
title: EM_SETSTORYTYPE Meldung (RichEdit. h)
description: Legt den Texttyp fest.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- Windows-Steuerelemente für EM_SETSTORYTYPE Meldung
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858789"
---
# <a name="em_setstorytype-message"></a><span data-ttu-id="e5ccd-104">EM \_ setstorytype-Meldung</span><span class="sxs-lookup"><span data-stu-id="e5ccd-104">EM\_SETSTORYTYPE message</span></span>

<span data-ttu-id="e5ccd-105">Legt den Texttyp fest.</span><span class="sxs-lookup"><span data-stu-id="e5ccd-105">Sets the story type.</span></span>


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a><span data-ttu-id="e5ccd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5ccd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5ccd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5ccd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5ccd-108">Der Story-Index.</span><span class="sxs-lookup"><span data-stu-id="e5ccd-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="e5ccd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5ccd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5ccd-110">Der neue Story-Typ.</span><span class="sxs-lookup"><span data-stu-id="e5ccd-110">The new story type.</span></span> <span data-ttu-id="e5ccd-111">Eine Liste der Story-Typen finden Sie unter [**EM \_ getstorytype**](em-getstorytype.md).</span><span class="sxs-lookup"><span data-stu-id="e5ccd-111">For a list of story types, see [**EM\_GETSTORYTYPE**](em-getstorytype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5ccd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5ccd-112">Return value</span></span>

<span data-ttu-id="e5ccd-113">Der Texttyp, der festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="e5ccd-113">The story type that was set.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ccd-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5ccd-114">Requirements</span></span>



| <span data-ttu-id="e5ccd-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5ccd-115">Requirement</span></span> | <span data-ttu-id="e5ccd-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e5ccd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ccd-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5ccd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e5ccd-118">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5ccd-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e5ccd-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5ccd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e5ccd-120">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5ccd-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5ccd-121">Header</span><span class="sxs-lookup"><span data-stu-id="e5ccd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5ccd-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ccd-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





