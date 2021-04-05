---
title: SB_GETTIPTEXT Meldung (kommstrg. h)
description: Ruft den QuickInfo-Text für einen Teil in einer Statusleiste ab. Die Statusleiste muss mit dem SBT- \_ Tooltips-Stil erstellt werden, um Quick Infos zu aktivieren.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- Windows-Steuerelemente für SB_GETTIPTEXT Meldung
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859108"
---
# <a name="sb_gettiptext-message"></a><span data-ttu-id="6d705-105">SB \_ GetTipText-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6d705-105">SB\_GETTIPTEXT message</span></span>

<span data-ttu-id="6d705-106">Ruft den QuickInfo-Text für einen Teil in einer Statusleiste ab.</span><span class="sxs-lookup"><span data-stu-id="6d705-106">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="6d705-107">Die Statusleiste muss mit dem [**SBT- \_ Tooltips**](status-bar-styles.md) -Stil erstellt werden, um Quick Infos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6d705-107">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d705-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d705-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d705-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d705-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d705-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den NULL basierten Index des Teils an, der den QuickInfo-Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="6d705-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the part that receives the tooltip text.</span></span> <span data-ttu-id="6d705-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die Größe des Puffers bei *LPARAM* in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="6d705-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the size of the buffer at *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="6d705-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d705-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d705-113">Ein Zeiger auf einen Zeichen Puffer, der den QuickInfo-Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="6d705-113">Pointer to a character buffer that receives the tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d705-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d705-114">Return value</span></span>

<span data-ttu-id="6d705-115">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d705-115">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d705-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d705-116">Remarks</span></span>

<span data-ttu-id="6d705-117">**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies zu Problemen bei der Anwendung führen.</span><span class="sxs-lookup"><span data-stu-id="6d705-117">**Security Warning:** Using this message incorrectly can cause problems for your application.</span></span> <span data-ttu-id="6d705-118">Wenn der Text z. b. zu groß für den *LPARAM* -Puffer ist, kann dies zu einem Pufferüberlauf führen.</span><span class="sxs-lookup"><span data-stu-id="6d705-118">For example, if the text is too large for the *lParam* buffer, it could cause a buffer overflow.</span></span> <span data-ttu-id="6d705-119">Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="6d705-119">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d705-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d705-120">Requirements</span></span>



| <span data-ttu-id="6d705-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d705-121">Requirement</span></span> | <span data-ttu-id="6d705-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6d705-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d705-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d705-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6d705-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d705-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d705-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d705-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6d705-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d705-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d705-127">Header</span><span class="sxs-lookup"><span data-stu-id="6d705-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d705-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d705-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6d705-129">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="6d705-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6d705-130">**SB \_ Gettiptextw** (Unicode) und **SB \_ gettiptexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6d705-130">**SB\_GETTIPTEXTW** (Unicode) and **SB\_GETTIPTEXTA** (ANSI)</span></span><br/>               |



 

