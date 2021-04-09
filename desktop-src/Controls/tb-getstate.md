---
title: TB_GETSTATE Meldung (kommstrg. h)
description: Ruft Informationen zum Zustand der angegebenen Schaltfläche in einer Symbolleiste ab, z. b. ob Sie aktiviert, gedrückt oder aktiviert ist.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- Windows-Steuerelemente für TB_GETSTATE Meldung
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858731"
---
# <a name="tb_getstate-message"></a><span data-ttu-id="e4d73-104">TB \_ GetState-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e4d73-104">TB\_GETSTATE message</span></span>

<span data-ttu-id="e4d73-105">Ruft Informationen zum Zustand der angegebenen Schaltfläche in einer Symbolleiste ab, z. b. ob Sie aktiviert, gedrückt oder aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e4d73-105">Retrieves information about the state of the specified button in a toolbar, such as whether it is enabled, pressed, or checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4d73-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4d73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4d73-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4d73-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d73-108">Der Befehls Bezeichner der Schaltfläche, für die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4d73-108">Command identifier of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="e4d73-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4d73-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e4d73-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e4d73-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4d73-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4d73-111">Return value</span></span>

<span data-ttu-id="e4d73-112">Gibt die Schaltflächen Zustandsinformationen zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="e4d73-112">Returns the button state information if successful, or -1 otherwise.</span></span> <span data-ttu-id="e4d73-113">Die Schaltflächen Zustandsinformationen können eine Kombination der Werte sein, die in den Symbolleisten- [**Schaltflächen Zuständen**](toolbar-button-states.md)aufgeführt sind</span><span class="sxs-lookup"><span data-stu-id="e4d73-113">The button state information can be a combination of the values listed in [**Toolbar Button States**](toolbar-button-states.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d73-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4d73-114">Requirements</span></span>



| <span data-ttu-id="e4d73-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4d73-115">Requirement</span></span> | <span data-ttu-id="e4d73-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e4d73-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d73-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4d73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4d73-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4d73-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4d73-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4d73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4d73-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4d73-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4d73-121">Header</span><span class="sxs-lookup"><span data-stu-id="e4d73-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4d73-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4d73-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





