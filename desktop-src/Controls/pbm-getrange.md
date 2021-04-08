---
title: PBM_GETRANGE Meldung (kommstrg. h)
description: Ruft Informationen über die aktuellen höchst-und tiefstgrenzen eines angegebenen Statusanzeige-Steuer Elements ab.
ms.assetid: 676b7a37-bdde-4307-9888-9a0cf40db2db
keywords:
- Windows-Steuerelemente für PBM_GETRANGE Meldung
topic_type:
- apiref
api_name:
- PBM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c4ffe9365686432a5e78cb1540055f41a838fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956814"
---
# <a name="pbm_getrange-message"></a><span data-ttu-id="f537e-104">PBM- \_ GetRange-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f537e-104">PBM\_GETRANGE message</span></span>

<span data-ttu-id="f537e-105">Ruft Informationen über die aktuellen höchst-und tiefstgrenzen eines angegebenen Statusanzeige-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="f537e-105">Retrieves information about the current high and low limits of a given progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f537e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f537e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f537e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f537e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f537e-108">Flagwert, der angibt, welcher Grenzwert als Rückgabewert der Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f537e-108">Flag value specifying which limit value is to be used as the message's return value.</span></span> <span data-ttu-id="f537e-109">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="f537e-109">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="f537e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f537e-110">Value</span></span>                                                                                                                                    | <span data-ttu-id="f537e-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f537e-111">Meaning</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="f537e-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="f537e-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="f537e-113">Gibt den unteren Grenzwert zurück.</span><span class="sxs-lookup"><span data-stu-id="f537e-113">Return the low limit.</span></span><br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="f537e-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="f537e-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="f537e-115">Gibt die Obergrenze zurück.</span><span class="sxs-lookup"><span data-stu-id="f537e-115">Return the high limit.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f537e-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f537e-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f537e-117">Zeiger auf eine [**pbrange**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) -Struktur, die mit den höchst-und tiefstgrenzen des Statusanzeige-Steuer Elements aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f537e-117">Pointer to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with the high and low limits of the progress bar control.</span></span> <span data-ttu-id="f537e-118">Wenn dieser Parameter auf **null** festgelegt ist, gibt das Steuerelement nur das von *wParam* angegebene Limit zurück.</span><span class="sxs-lookup"><span data-stu-id="f537e-118">If this parameter is set to **NULL**, the control will return only the limit specified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f537e-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f537e-119">Return value</span></span>

<span data-ttu-id="f537e-120">Gibt einen int-Wert zurück, der den von *wParam* angegebenen Grenzwert darstellt.</span><span class="sxs-lookup"><span data-stu-id="f537e-120">Returns an INT that represents the limit value specified by *wParam*.</span></span> <span data-ttu-id="f537e-121">Wenn *LPARAM* nicht **null** ist, muss *LPARAM* auf eine [**pbrange**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) -Struktur verweisen, die mit beiden Limit-Werten gefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f537e-121">If *lParam* is not **NULL**, *lParam* must point to a [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) structure that is to be filled with both limit values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f537e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f537e-122">Requirements</span></span>



| <span data-ttu-id="f537e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f537e-123">Requirement</span></span> | <span data-ttu-id="f537e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f537e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f537e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f537e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f537e-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f537e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f537e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f537e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f537e-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f537e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f537e-129">Header</span><span class="sxs-lookup"><span data-stu-id="f537e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f537e-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f537e-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





