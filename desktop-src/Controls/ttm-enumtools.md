---
title: TTM_ENUMTOOLS Nachricht (Commctrl.h)
description: Ruft die Informationen ab, die ein QuickInfo-Steuerelement über das aktuelle Tool \ 8212 verwaltet, d. h. das Tool, für das die QuickInfo derzeit Text anzeigt.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- TTM_ENUMTOOLS Meldung Windows-Steuerelemente
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
ms.openlocfilehash: a67f23a145838aa3562c81e78fb82c3ea66320df
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327135"
---
# <a name="ttm_enumtools-message"></a><span data-ttu-id="e8e54-104">\_TTM-ENUMTOOLS-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e8e54-104">TTM\_ENUMTOOLS message</span></span>

<span data-ttu-id="e8e54-105">Ruft die Informationen ab, die ein QuickInfo-Steuerelement über das aktuelle Tool verwaltet, d. h. das Tool, für das die QuickInfo derzeit Text anzeigt.</span><span class="sxs-lookup"><span data-stu-id="e8e54-105">Retrieves the information that a tooltip control maintains about the current tool that is, the tool for which the tooltip is currently displaying text.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8e54-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8e54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8e54-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8e54-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e54-108">Nullbasierter Index des Tools, für das Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e8e54-108">Zero-based index of the tool for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="e8e54-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8e54-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8e54-110">Zeiger auf eine [**TOOLINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) die Informationen über das Tool empfängt.</span><span class="sxs-lookup"><span data-stu-id="e8e54-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the tool.</span></span> <span data-ttu-id="e8e54-111">Legen Sie den **cbSize-Member** dieser Struktur vor dem Senden dieser Nachricht auf sizeof(TOOLINFO) fest.</span><span class="sxs-lookup"><span data-stu-id="e8e54-111">Set the **cbSize** member of this structure to sizeof(TOOLINFO) before sending this message.</span></span> <span data-ttu-id="e8e54-112">Zuordnen eines Puffers.</span><span class="sxs-lookup"><span data-stu-id="e8e54-112">Allocate a buffer.</span></span> <span data-ttu-id="e8e54-113">Legen Sie den **lpszText-Member** so fest, dass er auf den Puffer verweist, um den Tooltext zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="e8e54-113">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span> <span data-ttu-id="e8e54-114">Es gibt keine Möglichkeit, die erforderliche Puffergröße zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e8e54-114">There is no way to determine the required buffer size.</span></span> <span data-ttu-id="e8e54-115">Tooltext, wie er am **lpszText-Member** der **TOOLINFO-Struktur** zurückgegeben wird, hat jedoch eine maximale Länge von 80 **TCHARs,** einschließlich des abschließenden **NULL-Werts.**</span><span class="sxs-lookup"><span data-stu-id="e8e54-115">However, tool text, as returned at the **lpszText** member of the **TOOLINFO** structure, has a maximum length of 80 **TCHARs**, including the terminating **NULL**.</span></span> <span data-ttu-id="e8e54-116">Wenn der Text diese Länge überschreitet, wird er abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="e8e54-116">If the text exceeds this length, it is truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8e54-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8e54-117">Return value</span></span>

<span data-ttu-id="e8e54-118">Gibt **FALSE** zurück, unabhängig davon, ob ein Tool aufzählt wurde.</span><span class="sxs-lookup"><span data-stu-id="e8e54-118">Returns **FALSE** whether or not a tool was enumerated.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8e54-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e8e54-119">Remarks</span></span>

<span data-ttu-id="e8e54-120">**Sicherheitswarnung:** Die Verwendung dieser Meldung kann die Sicherheit Ihres Programms gefährden.</span><span class="sxs-lookup"><span data-stu-id="e8e54-120">**Security Warning:** Using this message might compromise the security of your program.</span></span> <span data-ttu-id="e8e54-121">Diese Nachricht bietet keine Möglichkeit für den Nachrichtenempfänger, die Größe des Puffers zu kennen oder die Größe des Puffers anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e8e54-121">This message does not provide a way for the message receiver to know the size of the buffer or to specify the size of the buffer.</span></span> <span data-ttu-id="e8e54-122">Lesen Sie die [Sicherheitsüberlegungen: Microsoft Windows-Steuerelemente,](sec-comctls.md) bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="e8e54-122">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e54-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8e54-123">Requirements</span></span>



| <span data-ttu-id="e8e54-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8e54-124">Requirement</span></span> | <span data-ttu-id="e8e54-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e8e54-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e54-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8e54-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e54-127">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8e54-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8e54-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8e54-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e54-129">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8e54-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8e54-130">Header</span><span class="sxs-lookup"><span data-stu-id="e8e54-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e54-131"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e54-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e8e54-132">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e8e54-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e8e54-133">**TTM \_ ENUMTOOLSW** (Unicode) und **TTM \_ ENUMTOOLSA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e8e54-133">**TTM\_ENUMTOOLSW** (Unicode) and **TTM\_ENUMTOOLSA** (ANSI)</span></span><br/>               |



 

 





