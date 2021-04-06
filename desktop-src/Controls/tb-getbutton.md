---
title: TB_GETBUTTON Meldung (kommstrg. h)
description: Ruft Informationen über die angegebene Schaltfläche in einer Symbolleiste ab.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- Windows-Steuerelemente für TB_GETBUTTON Meldung
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2080a6c984bb2384f68a1388bd46fe598f5087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743961"
---
# <a name="tb_getbutton-message"></a><span data-ttu-id="f97ce-104">TB \_ getbutton-Meldung</span><span class="sxs-lookup"><span data-stu-id="f97ce-104">TB\_GETBUTTON message</span></span>

<span data-ttu-id="f97ce-105">Ruft Informationen über die angegebene Schaltfläche in einer Symbolleiste ab.</span><span class="sxs-lookup"><span data-stu-id="f97ce-105">Retrieves information about the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f97ce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f97ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f97ce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f97ce-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f97ce-108">NULL basierter Index der Schaltfläche, für die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f97ce-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="f97ce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f97ce-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f97ce-110">Ein Zeiger auf die [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur, die die Schaltflächen Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="f97ce-110">Pointer to the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that receives the button information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f97ce-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f97ce-111">Return value</span></span>

<span data-ttu-id="f97ce-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="f97ce-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f97ce-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f97ce-113">Requirements</span></span>



| <span data-ttu-id="f97ce-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f97ce-114">Requirement</span></span> | <span data-ttu-id="f97ce-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f97ce-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f97ce-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f97ce-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f97ce-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f97ce-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f97ce-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f97ce-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f97ce-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f97ce-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f97ce-120">Header</span><span class="sxs-lookup"><span data-stu-id="f97ce-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f97ce-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f97ce-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





