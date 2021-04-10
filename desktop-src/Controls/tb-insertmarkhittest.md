---
title: TB_INSERTMARKHITTEST Meldung (kommstrg. h)
description: Ruft die einfügemarkierungsinformationen für einen Punkt in einer Symbolleiste ab.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- Windows-Steuerelemente für TB_INSERTMARKHITTEST Meldung
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040432"
---
# <a name="tb_insertmarkhittest-message"></a><span data-ttu-id="3b212-104">TB \_ insertmarkhittest-Meldung</span><span class="sxs-lookup"><span data-stu-id="3b212-104">TB\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="3b212-105">Ruft die einfügemarkierungsinformationen für einen Punkt in einer Symbolleiste ab.</span><span class="sxs-lookup"><span data-stu-id="3b212-105">Retrieves the insertion mark information for a point in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b212-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b212-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b212-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b212-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b212-108">Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die die Treffer Test Koordinaten relativ zum Client Bereich der Symbolleiste enthält.</span><span class="sxs-lookup"><span data-stu-id="3b212-108">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the hit test coordinates, relative to the client area of the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="3b212-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b212-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3b212-110">Ein Zeiger auf eine [**tbinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) -Struktur, die die einfügemarkierungsinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="3b212-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b212-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b212-111">Return value</span></span>

<span data-ttu-id="3b212-112">Gibt einen Wert ungleich 0 (null) zurück, wenn der Punkt eine Einfügemarke ist, andernfalls NULL</span><span class="sxs-lookup"><span data-stu-id="3b212-112">Returns nonzero if the point is an insertion mark, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b212-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b212-113">Requirements</span></span>



| <span data-ttu-id="3b212-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b212-114">Requirement</span></span> | <span data-ttu-id="3b212-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3b212-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b212-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b212-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3b212-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b212-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b212-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b212-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3b212-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b212-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b212-120">Header</span><span class="sxs-lookup"><span data-stu-id="3b212-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b212-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b212-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

