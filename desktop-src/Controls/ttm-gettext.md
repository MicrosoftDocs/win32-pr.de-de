---
title: TTM_GETTEXT Meldung (kommstrg. h)
description: Ruft die Informationen ab, die ein QuickInfo-Steuerelement zu einem Tool beibehält.
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- Windows-Steuerelemente für TTM_GETTEXT Meldung
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337515"
---
# <a name="ttm_gettext-message"></a><span data-ttu-id="c54e0-104">TTM \_ gettext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c54e0-104">TTM\_GETTEXT message</span></span>

<span data-ttu-id="c54e0-105">Ruft die Informationen ab, die ein QuickInfo-Steuerelement zu einem Tool beibehält.</span><span class="sxs-lookup"><span data-stu-id="c54e0-105">Retrieves the information a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="c54e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c54e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c54e0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c54e0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c54e0-108">Die Anzahl der **tchars**, einschließlich des abschließenden **null**-Werts, der in den Puffer kopiert werden soll, auf den von **lpszText** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c54e0-108">The number of **TCHARs**, including the terminating **NULL**, to copy to the buffer pointed to by **lpszText**.</span></span> </dd> <dt>

<span data-ttu-id="c54e0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c54e0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c54e0-110">Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c54e0-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="c54e0-111">Legen Sie den **CBSIZE** -Member dieser-Struktur auf fest, `sizeof(TOOLINFO)` bevor Sie diese Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="c54e0-111">Set the **cbSize** member of this structure to `sizeof(TOOLINFO)` before sending this message.</span></span> <span data-ttu-id="c54e0-112">Legen Sie die **HWND** -und **UID** -Member fest, um das Tool zu identifizieren, für das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c54e0-112">Set the **hwnd** and **uId** members to identify the tool for which to retrieve information.</span></span> <span data-ttu-id="c54e0-113">Zuordnen eines Puffer der Größe, die von *wParam* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c54e0-113">Allocate a buffer of size specified by *wParam*.</span></span> <span data-ttu-id="c54e0-114">Legen Sie fest, dass der **lpszText** -Member auf den Puffer verweist, um den tooltext zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c54e0-114">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c54e0-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c54e0-115">Return value</span></span>

<span data-ttu-id="c54e0-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="c54e0-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c54e0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c54e0-117">Requirements</span></span>



| <span data-ttu-id="c54e0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c54e0-118">Requirement</span></span> | <span data-ttu-id="c54e0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c54e0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c54e0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c54e0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c54e0-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c54e0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c54e0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c54e0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c54e0-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c54e0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c54e0-124">Header</span><span class="sxs-lookup"><span data-stu-id="c54e0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c54e0-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c54e0-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c54e0-126">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c54e0-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c54e0-127">**TTM \_ Gettextw** (Unicode) und **TTM \_ gettexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c54e0-127">**TTM\_GETTEXTW** (Unicode) and **TTM\_GETTEXTA** (ANSI)</span></span><br/>                   |



 

 





