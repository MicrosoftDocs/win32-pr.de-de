---
title: TB_GETHOTITEM Meldung (kommstrg. h)
description: Ruft den Index des aktiven Elements auf einer Symbolleiste ab.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- Windows-Steuerelemente für TB_GETHOTITEM Meldung
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829864cc9223ba15b49b1ecc623f294fd4a6b4fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476302"
---
# <a name="tb_gethotitem-message"></a><span data-ttu-id="a6455-104">TB- \_ gethotitem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a6455-104">TB\_GETHOTITEM message</span></span>

<span data-ttu-id="a6455-105">Ruft den Index des aktiven Elements auf einer Symbolleiste ab.</span><span class="sxs-lookup"><span data-stu-id="a6455-105">Retrieves the index of the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6455-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6455-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6455-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6455-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a6455-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a6455-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a6455-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6455-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a6455-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a6455-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6455-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6455-111">Return value</span></span>

<span data-ttu-id="a6455-112">Gibt den Index des aktiven Elements oder-1 zurück, wenn kein heißes Element festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a6455-112">Returns the index of the hot item, or -1 if no hot item is set.</span></span> <span data-ttu-id="a6455-113">Symbolleisten-Steuerelemente, die nicht über den [**\_ flachen tbstyle**](toolbar-control-and-button-styles.md) -Stil verfügen, verfügen nicht über heiße Elemente.</span><span class="sxs-lookup"><span data-stu-id="a6455-113">Toolbar controls that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style do not have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6455-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6455-114">Requirements</span></span>



| <span data-ttu-id="a6455-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6455-115">Requirement</span></span> | <span data-ttu-id="a6455-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a6455-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6455-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6455-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a6455-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6455-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6455-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6455-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a6455-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6455-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6455-121">Header</span><span class="sxs-lookup"><span data-stu-id="a6455-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6455-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6455-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





