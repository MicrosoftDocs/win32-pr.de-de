---
title: EM_EXLINEFROMCHAR Meldung (RichEdit. h)
description: Bestimmt, welche Zeile das angegebene Zeichen in einem Rich-Edit-Steuerelement enthält.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- Windows-Steuerelemente für EM_EXLINEFROMCHAR Meldung
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce904725c5dc63732bae07cfaa95b41558db11d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479466"
---
# <a name="em_exlinefromchar-message"></a><span data-ttu-id="7196d-104">EM \_ exlinefromchar-Meldung</span><span class="sxs-lookup"><span data-stu-id="7196d-104">EM\_EXLINEFROMCHAR message</span></span>

<span data-ttu-id="7196d-105">Bestimmt, welche Zeile das angegebene Zeichen in einem Rich-Edit-Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="7196d-105">Determines which line contains the specified character in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7196d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7196d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7196d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7196d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7196d-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7196d-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7196d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7196d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7196d-110">NULL basierter Index des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="7196d-110">Zero-based index of the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7196d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7196d-111">Return value</span></span>

<span data-ttu-id="7196d-112">Diese Meldung gibt den NULL basierten Index der Zeile zurück.</span><span class="sxs-lookup"><span data-stu-id="7196d-112">This message returns the zero-based index of the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="7196d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7196d-113">Requirements</span></span>



| <span data-ttu-id="7196d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7196d-114">Requirement</span></span> | <span data-ttu-id="7196d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7196d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7196d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7196d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7196d-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7196d-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7196d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7196d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7196d-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7196d-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7196d-120">Header</span><span class="sxs-lookup"><span data-stu-id="7196d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7196d-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7196d-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





