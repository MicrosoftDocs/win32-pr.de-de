---
title: TTM_ENUMTOOLS Meldung (kommstrg. h)
description: Ruft die Informationen ab, die ein QuickInfo-Steuerelement über das aktuelle Tool \ 8212 verwaltet, d. h. das Tool, für das die QuickInfo momentan Text anzeigt.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- Windows-Steuerelemente für TTM_ENUMTOOLS Meldung
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad1679f9740539507a57c4cba93319569add0af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476791"
---
# <a name="ttm_enumtools-message"></a><span data-ttu-id="a8ba0-104">TTM- \_ enumtoolsnachricht</span><span class="sxs-lookup"><span data-stu-id="a8ba0-104">TTM\_ENUMTOOLS message</span></span>

<span data-ttu-id="a8ba0-105">Ruft die Informationen ab, die ein QuickInfo-Steuerelement über das aktuelle Tool, das Tool, für das die QuickInfo aktuell Text anzeigt, verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-105">Retrieves the information that a tooltip control maintains about the current tool that is, the tool for which the tooltip is currently displaying text.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8ba0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8ba0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8ba0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8ba0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ba0-108">Der null basierte Index des Tools, für das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-108">Zero-based index of the tool for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="a8ba0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8ba0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ba0-110">Ein Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die Informationen über das Tool empfängt.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the tool.</span></span> <span data-ttu-id="a8ba0-111">Legen Sie den **CBSIZE** -Member dieser Struktur auf sizeof (toolinfo) fest, bevor Sie diese Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-111">Set the **cbSize** member of this structure to sizeof(TOOLINFO) before sending this message.</span></span> <span data-ttu-id="a8ba0-112">Zuordnen eines Puffers.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-112">Allocate a buffer.</span></span> <span data-ttu-id="a8ba0-113">Legen Sie fest, dass der **lpszText** -Member auf den Puffer verweist, um den tooltext zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-113">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span> <span data-ttu-id="a8ba0-114">Es gibt keine Möglichkeit, die erforderliche Puffergröße zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-114">There is no way to determine the required buffer size.</span></span> <span data-ttu-id="a8ba0-115">Allerdings hat der Tool Text, wie er im **lpszText** -Member der **toolinfo** -Struktur zurückgegeben wird, eine maximale Länge von 80 **tchars**, einschließlich des abschließenden **null**-Werts.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-115">However, tool text, as returned at the **lpszText** member of the **TOOLINFO** structure, has a maximum length of 80 **TCHARs**, including the terminating **NULL**.</span></span> <span data-ttu-id="a8ba0-116">Wenn der Text diese Länge überschreitet, wird er abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-116">If the text exceeds this length, it is truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8ba0-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8ba0-117">Return value</span></span>

<span data-ttu-id="a8ba0-118">Gibt **true** zurück, wenn Tools aufgelistet werden, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="a8ba0-118">Returns **TRUE** if any tools are enumerated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8ba0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8ba0-119">Remarks</span></span>

<span data-ttu-id="a8ba0-120">**Sicherheitswarnung:** Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-120">**Security Warning:** Using this message might compromise the security of your program.</span></span> <span data-ttu-id="a8ba0-121">Diese Meldung bietet keine Möglichkeit, dass der Nachrichtenempfänger die Größe des Puffers kennt oder die Größe des Puffers angibt.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-121">This message does not provide a way for the message receiver to know the size of the buffer or to specify the size of the buffer.</span></span> <span data-ttu-id="a8ba0-122">Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="a8ba0-122">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ba0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8ba0-123">Requirements</span></span>



| <span data-ttu-id="a8ba0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8ba0-124">Requirement</span></span> | <span data-ttu-id="a8ba0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a8ba0-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ba0-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8ba0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a8ba0-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8ba0-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a8ba0-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8ba0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a8ba0-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8ba0-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a8ba0-130">Header</span><span class="sxs-lookup"><span data-stu-id="a8ba0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8ba0-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8ba0-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a8ba0-132">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a8ba0-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a8ba0-133">**TTM \_ Enumtoolsw** (Unicode) und **TTM \_ enumtoolsa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a8ba0-133">**TTM\_ENUMTOOLSW** (Unicode) and **TTM\_ENUMTOOLSA** (ANSI)</span></span><br/>               |



 

 





