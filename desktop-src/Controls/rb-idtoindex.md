---
title: RB_IDTOINDEX Meldung (kommstrg. h)
description: Konvertiert einen Band Bezeichner in einen Band-Index in einem Grund leisten-Steuerelement.
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- Windows-Steuerelemente für RB_IDTOINDEX Meldung
topic_type:
- apiref
api_name:
- RB_IDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7acd85862bc4787a6b32d2fdd3c897a52913b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475345"
---
# <a name="rb_idtoindex-message"></a><span data-ttu-id="9319c-104">RB \_ iddeindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="9319c-104">RB\_IDTOINDEX message</span></span>

<span data-ttu-id="9319c-105">Konvertiert einen Band Bezeichner in einen Band-Index in einem Grund leisten-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9319c-105">Converts a band identifier to a band index in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9319c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9319c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9319c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9319c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9319c-108">Der von der Anwendung definierte Bezeichner des fraglichen Bands.</span><span class="sxs-lookup"><span data-stu-id="9319c-108">The application-defined identifier of the band in question.</span></span> <span data-ttu-id="9319c-109">Dies ist der Wert, der beim Einfügen des Bands im **wID** -Member der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur weitergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9319c-109">This is the value that was passed in the **wID** member of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure when the band was inserted.</span></span>

</dd> <dt>

<span data-ttu-id="9319c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9319c-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9319c-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9319c-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9319c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9319c-112">Return value</span></span>

<span data-ttu-id="9319c-113">Gibt den NULL basierten BandIndex zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="9319c-113">Returns the zero-based band index if successful, or -1 otherwise.</span></span> <span data-ttu-id="9319c-114">Wenn doppelte Band Bezeichner vorhanden sind, wird der erste zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9319c-114">If duplicate band identifiers exist, the first one is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="9319c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9319c-115">Requirements</span></span>



| <span data-ttu-id="9319c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9319c-116">Requirement</span></span> | <span data-ttu-id="9319c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9319c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9319c-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9319c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9319c-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9319c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9319c-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9319c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9319c-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9319c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9319c-122">Header</span><span class="sxs-lookup"><span data-stu-id="9319c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9319c-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9319c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





