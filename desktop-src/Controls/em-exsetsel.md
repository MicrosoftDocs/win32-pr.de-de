---
title: EM_EXSETSEL Meldung (RichEdit. h)
description: Wählt einen Bereich von Zeichen oder Component Object Model (com)-Objekten in einem Rich-Edit-Steuerelement von Microsoft aus.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- Windows-Steuerelemente für EM_EXSETSEL Meldung
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859018"
---
# <a name="em_exsetsel-message"></a><span data-ttu-id="016f2-104">EM \_ Ex-tsel-Meldung</span><span class="sxs-lookup"><span data-stu-id="016f2-104">EM\_EXSETSEL message</span></span>

<span data-ttu-id="016f2-105">Wählt einen Bereich von Zeichen oder Component Object Model (com)-Objekten in einem Rich-Edit-Steuerelement von Microsoft aus.</span><span class="sxs-lookup"><span data-stu-id="016f2-105">Selects a range of characters or Component Object Model (COM) objects in a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="016f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="016f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="016f2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="016f2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="016f2-108">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="016f2-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="016f2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="016f2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="016f2-110">Eine [**charrange**](/windows/desktop/api/Richedit/ns-richedit-charrange) -Struktur, die den Auswahlbereich angibt.</span><span class="sxs-lookup"><span data-stu-id="016f2-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that specifies the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="016f2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="016f2-111">Return value</span></span>

<span data-ttu-id="016f2-112">Der Rückgabewert ist die Auswahl, die tatsächlich festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="016f2-112">The return value is the selection that is actually set.</span></span>

## <a name="requirements"></a><span data-ttu-id="016f2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="016f2-113">Requirements</span></span>



| <span data-ttu-id="016f2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="016f2-114">Requirement</span></span> | <span data-ttu-id="016f2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="016f2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="016f2-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="016f2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="016f2-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="016f2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="016f2-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="016f2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="016f2-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="016f2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="016f2-120">Header</span><span class="sxs-lookup"><span data-stu-id="016f2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="016f2-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="016f2-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





