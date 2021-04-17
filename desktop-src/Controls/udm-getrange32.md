---
title: UDM_GETRANGE32 Meldung (kommstrg. h)
description: Ruft den 32-Bit-Bereich eines auf-ab-Steuer Elements ab.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- Windows-Steuerelemente für UDM_GETRANGE32 Meldung
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476290"
---
# <a name="udm_getrange32-message"></a><span data-ttu-id="bd38a-104">UDM \_ GETRANGE32 Meldung</span><span class="sxs-lookup"><span data-stu-id="bd38a-104">UDM\_GETRANGE32 message</span></span>

<span data-ttu-id="bd38a-105">Ruft den 32-Bit-Bereich eines auf-ab-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="bd38a-105">Retrieves the 32-bit range of an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd38a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd38a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd38a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd38a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd38a-108">Ein Zeiger auf eine Ganzzahl mit Vorzeichen, die die Untergrenze des auf-ab-Steuerelement Bereichs empfängt.</span><span class="sxs-lookup"><span data-stu-id="bd38a-108">Pointer to a signed integer that receives the lower limit of the up-down control range.</span></span> <span data-ttu-id="bd38a-109">Dieser Parameter kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="bd38a-109">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bd38a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd38a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd38a-111">Ein Zeiger auf eine Ganzzahl mit Vorzeichen, die die Obergrenze des auf-ab-Steuerelement Bereichs empfängt.</span><span class="sxs-lookup"><span data-stu-id="bd38a-111">Pointer to a signed integer that receives the upper limit of the up-down control range.</span></span> <span data-ttu-id="bd38a-112">Dieser Parameter kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="bd38a-112">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd38a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd38a-113">Return value</span></span>

<span data-ttu-id="bd38a-114">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd38a-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd38a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd38a-115">Requirements</span></span>



| <span data-ttu-id="bd38a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd38a-116">Requirement</span></span> | <span data-ttu-id="bd38a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bd38a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd38a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd38a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd38a-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd38a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd38a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd38a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd38a-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd38a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd38a-122">Header</span><span class="sxs-lookup"><span data-stu-id="bd38a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd38a-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd38a-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





