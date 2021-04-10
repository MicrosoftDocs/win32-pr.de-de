---
title: TB_GETOBJECT Meldung (kommstrg. h)
description: Ruft das IDropTarget-Element für ein ToolBar-Steuerelement ab.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- Windows-Steuerelemente für TB_GETOBJECT Meldung
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105056"
---
# <a name="tb_getobject-message"></a><span data-ttu-id="ea8f2-104">TB- \_ GetObject-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ea8f2-104">TB\_GETOBJECT message</span></span>

<span data-ttu-id="ea8f2-105">Ruft das [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Element für ein ToolBar-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-105">Retrieves the [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea8f2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea8f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8f2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea8f2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea8f2-108">Der Bezeichner der angeforderten Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-108">Identifier of the interface being requested.</span></span> <span data-ttu-id="ea8f2-109">Dieser Wert muss auf **IID \_ IDropTarget** zeigen.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-109">This value must point to **IID\_IDropTarget**.</span></span>

</dd> <dt>

<span data-ttu-id="ea8f2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea8f2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea8f2-111">Adresse, die den Schnittstellen Zeiger empfängt.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-111">Address that receives the interface pointer.</span></span> <span data-ttu-id="ea8f2-112">Wenn ein Fehler auftritt, wird ein **null** -Zeiger in diese Adresse eingefügt.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-112">If an error occurs, a **NULL** pointer is placed in this address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea8f2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea8f2-113">Return value</span></span>

<span data-ttu-id="ea8f2-114">Gibt einen **HRESULT** -Wert zurück, der den Erfolg oder das Fehlschlagen des Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-114">Returns an **HRESULT** value indicating success or failure of the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea8f2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea8f2-115">Remarks</span></span>

<span data-ttu-id="ea8f2-116">Das [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) der Symbolleiste wird von der Symbolleiste verwendet, wenn Objekte gezogen oder darauf abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ea8f2-116">The toolbar's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) is used by the toolbar when objects are dragged over or dropped onto it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8f2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea8f2-117">Requirements</span></span>



| <span data-ttu-id="ea8f2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea8f2-118">Requirement</span></span> | <span data-ttu-id="ea8f2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ea8f2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8f2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea8f2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ea8f2-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea8f2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea8f2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea8f2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ea8f2-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea8f2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea8f2-124">Header</span><span class="sxs-lookup"><span data-stu-id="ea8f2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea8f2-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea8f2-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

