---
title: CBEM_SETITEM Meldung (kommstrg. h)
description: Legt die Attribute für ein Element in einem ComboBoxEx-Steuerelement fest.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- Windows-Steuerelemente für CBEM_SETITEM Meldung
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743400"
---
# <a name="cbem_setitem-message"></a><span data-ttu-id="20232-104">CBEM-Element \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="20232-104">CBEM\_SETITEM message</span></span>

<span data-ttu-id="20232-105">Legt die Attribute für ein Element in einem ComboBoxEx-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="20232-105">Sets the attributes for an item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="20232-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20232-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20232-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="20232-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="20232-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="20232-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="20232-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20232-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20232-110">Ein Zeiger auf eine [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) -Struktur, die die festzulegenden Element Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="20232-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains the item information to be set.</span></span> <span data-ttu-id="20232-111">Wenn die Nachricht gesendet wird, muss der **Mask** -Member der Struktur festgelegt werden, um anzugeben, welche Attribute gültig sind, und der **iItem** -Member muss den NULL basierten Index des zu ändernden Elements angeben.</span><span class="sxs-lookup"><span data-stu-id="20232-111">When the message is sent, the **mask** member of the structure must be set to indicate which attributes are valid and the **iItem** member must specify the zero-based index of the item to be modified.</span></span> <span data-ttu-id="20232-112">Wenn Sie den **iItem** -Member auf-1 festlegen, wird das im Bearbeitungs Steuerelement angezeigte Element geändert.</span><span class="sxs-lookup"><span data-stu-id="20232-112">Setting the **iItem** member to -1 will modify the item displayed in the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20232-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20232-113">Return value</span></span>

<span data-ttu-id="20232-114">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="20232-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="20232-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20232-115">Requirements</span></span>



| <span data-ttu-id="20232-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20232-116">Requirement</span></span> | <span data-ttu-id="20232-117">Wert</span><span class="sxs-lookup"><span data-stu-id="20232-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20232-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20232-118">Minimum supported client</span></span><br/> | <span data-ttu-id="20232-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20232-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20232-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20232-120">Minimum supported server</span></span><br/> | <span data-ttu-id="20232-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20232-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20232-122">Header</span><span class="sxs-lookup"><span data-stu-id="20232-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="20232-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="20232-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="20232-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="20232-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="20232-125">**CBEM \_** "CBEM" (Unicode) und " **CBEM \_** " (ANSI)</span><span class="sxs-lookup"><span data-stu-id="20232-125">**CBEM\_SETITEMW** (Unicode) and **CBEM\_SETITEMA** (ANSI)</span></span><br/>                 |



 

 





