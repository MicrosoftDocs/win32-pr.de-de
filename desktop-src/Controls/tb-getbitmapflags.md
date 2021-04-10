---
title: TB_GETBITMAPFLAGS Meldung (kommstrg. h)
description: Ruft die Flags ab, die den Typ der zu verwendenden Bitmap beschreiben.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- Windows-Steuerelemente für TB_GETBITMAPFLAGS Meldung
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106604"
---
# <a name="tb_getbitmapflags-message"></a><span data-ttu-id="458ed-104">TB \_ getbitmapflags-Nachricht</span><span class="sxs-lookup"><span data-stu-id="458ed-104">TB\_GETBITMAPFLAGS message</span></span>

<span data-ttu-id="458ed-105">Ruft die Flags ab, die den Typ der zu verwendenden Bitmap beschreiben.</span><span class="sxs-lookup"><span data-stu-id="458ed-105">Retrieves the flags that describe the type of bitmap to be used.</span></span>

## <a name="parameters"></a><span data-ttu-id="458ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="458ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="458ed-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="458ed-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="458ed-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="458ed-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="458ed-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="458ed-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="458ed-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="458ed-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="458ed-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="458ed-111">Return value</span></span>

<span data-ttu-id="458ed-112">Gibt einen **DWORD** -Wert zurück, der den Typ der zu verwendenden Bitmap beschreibt.</span><span class="sxs-lookup"><span data-stu-id="458ed-112">Returns a **DWORD** value that describes the type of bitmap that should be used.</span></span> <span data-ttu-id="458ed-113">Wenn für diesen Rückgabewert das große tbbf- \_ Flag festgelegt ist, sollten Anwendungen große Bitmaps (24 x 24) verwenden. andernfalls sollten Anwendungen kleine Bitmaps (16 x 16) verwenden.</span><span class="sxs-lookup"><span data-stu-id="458ed-113">If this return value has the TBBF\_LARGE flag set, applications should use large bitmaps (24 x 24); otherwise, applications should use small bitmaps (16 x 16).</span></span> <span data-ttu-id="458ed-114">Alle anderen Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="458ed-114">All other bits are reserved.</span></span>

## <a name="remarks"></a><span data-ttu-id="458ed-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="458ed-115">Remarks</span></span>

<span data-ttu-id="458ed-116">Der von **TB \_ getbitmapflags** zurückgegebene Wert ist nur eine Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="458ed-116">The value returned by **TB\_GETBITMAPFLAGS** is only advisory.</span></span> <span data-ttu-id="458ed-117">Das Symbolleisten-Steuerelement empfiehlt große oder kleine Bitmaps, je nachdem, ob der Benutzer große oder kleine Schriftarten ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="458ed-117">The toolbar control recommends large or small bitmaps based upon whether the user has chosen large or small fonts.</span></span>

## <a name="requirements"></a><span data-ttu-id="458ed-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="458ed-118">Requirements</span></span>



| <span data-ttu-id="458ed-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="458ed-119">Requirement</span></span> | <span data-ttu-id="458ed-120">Wert</span><span class="sxs-lookup"><span data-stu-id="458ed-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="458ed-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="458ed-121">Minimum supported client</span></span><br/> | <span data-ttu-id="458ed-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="458ed-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="458ed-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="458ed-123">Minimum supported server</span></span><br/> | <span data-ttu-id="458ed-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="458ed-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="458ed-125">Header</span><span class="sxs-lookup"><span data-stu-id="458ed-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="458ed-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="458ed-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





