---
title: RB_GETROWHEIGHT Meldung (kommstrg. h)
description: Ruft die Höhe einer angegebenen Zeile in einem Grund leisten-Steuerelement ab.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- Windows-Steuerelemente für RB_GETROWHEIGHT Meldung
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859050"
---
# <a name="rb_getrowheight-message"></a><span data-ttu-id="cae25-104">RB \_ getRowHeight-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cae25-104">RB\_GETROWHEIGHT message</span></span>

<span data-ttu-id="cae25-105">Ruft die Höhe einer angegebenen Zeile in einem Grund leisten-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="cae25-105">Retrieves the height of a specified row in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cae25-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cae25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae25-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cae25-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cae25-108">NULL basierter Index eines Bands.</span><span class="sxs-lookup"><span data-stu-id="cae25-108">Zero-based index of a band.</span></span> <span data-ttu-id="cae25-109">Die Höhe der Zeile, die das angegebene Band enthält, wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cae25-109">The height of the row that contains the specified band will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="cae25-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cae25-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cae25-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="cae25-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae25-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cae25-112">Return value</span></span>

<span data-ttu-id="cae25-113">Gibt einen **uint** -Wert zurück, der die Zeilenhöhe in Pixel darstellt.</span><span class="sxs-lookup"><span data-stu-id="cae25-113">Returns a **UINT** value that represents the row height, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae25-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cae25-114">Remarks</span></span>

<span data-ttu-id="cae25-115">Um die Anzahl der Zeilen in einem Grund leisten-Steuerelement abzurufen, verwenden Sie die [**RB \_ GetRowCount**](rb-getrowcount.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cae25-115">To retrieve the number of rows in a rebar control, use the [**RB\_GETROWCOUNT**](rb-getrowcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae25-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cae25-116">Requirements</span></span>



| <span data-ttu-id="cae25-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cae25-117">Requirement</span></span> | <span data-ttu-id="cae25-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cae25-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cae25-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cae25-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cae25-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cae25-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cae25-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cae25-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cae25-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cae25-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cae25-123">Header</span><span class="sxs-lookup"><span data-stu-id="cae25-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cae25-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cae25-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





