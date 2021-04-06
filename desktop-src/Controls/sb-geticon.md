---
title: SB_GETICON Meldung (kommstrg. h)
description: Ruft das Symbol für einen Teil in einer Statusleiste ab.
ms.assetid: f99508e3-afa8-48fd-b87a-fce41c4410ff
keywords:
- Windows-Steuerelemente für SB_GETICON Meldung
topic_type:
- apiref
api_name:
- SB_GETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab86809df54d796b8e83f05f2a2b9041450ce2fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859109"
---
# <a name="sb_geticon-message"></a><span data-ttu-id="19c75-104">SB- \_ GetIcon-Nachricht</span><span class="sxs-lookup"><span data-stu-id="19c75-104">SB\_GETICON message</span></span>

<span data-ttu-id="19c75-105">Ruft das Symbol für einen Teil in einer Statusleiste ab.</span><span class="sxs-lookup"><span data-stu-id="19c75-105">Retrieves the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="19c75-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19c75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19c75-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19c75-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19c75-108">NULL basierter Index des Teils, der das abzurufende Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="19c75-108">Zero-based index of the part that contains the icon to be retrieved.</span></span> <span data-ttu-id="19c75-109">Wenn dieser Parameter-1 ist, wird angenommen, dass es sich bei der Statusleiste um eine Statusleiste im [einfachen Modus](status-bars.md) handelt.</span><span class="sxs-lookup"><span data-stu-id="19c75-109">If this parameter is -1, the status bar is assumed to be a [Simple Mode](status-bars.md) status bar.</span></span>

</dd> <dt>

<span data-ttu-id="19c75-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19c75-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="19c75-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="19c75-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19c75-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19c75-112">Return value</span></span>

<span data-ttu-id="19c75-113">Gibt das Handle für das Symbol zurück, wenn erfolgreich, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="19c75-113">Returns the handle to the icon if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="19c75-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19c75-114">Requirements</span></span>



| <span data-ttu-id="19c75-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19c75-115">Requirement</span></span> | <span data-ttu-id="19c75-116">Wert</span><span class="sxs-lookup"><span data-stu-id="19c75-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19c75-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19c75-117">Minimum supported client</span></span><br/> | <span data-ttu-id="19c75-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19c75-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19c75-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19c75-119">Minimum supported server</span></span><br/> | <span data-ttu-id="19c75-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19c75-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19c75-121">Header</span><span class="sxs-lookup"><span data-stu-id="19c75-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="19c75-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="19c75-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





