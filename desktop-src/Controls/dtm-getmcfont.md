---
title: DTM_GETMCFONT Meldung (kommstrg. h)
description: Ruft die Schriftart ab, die das untergeordnete Monatskalender-Steuerelement des Datums-und Zeitauswahl Steuer Elements gegenwärtig verwendet. Sie können diese Nachricht explizit senden oder das "DateTime \_ getmonthcalfont"-Makro verwenden.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- Windows-Steuerelemente für DTM_GETMCFONT Meldung
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859178"
---
# <a name="dtm_getmcfont-message"></a><span data-ttu-id="545ad-105">DTM \_ getmcfont-Nachricht</span><span class="sxs-lookup"><span data-stu-id="545ad-105">DTM\_GETMCFONT message</span></span>

<span data-ttu-id="545ad-106">Ruft die Schriftart ab, die das untergeordnete Monatskalender-Steuerelement des Datums-und Zeitauswahl Steuer Elements gegenwärtig verwendet.</span><span class="sxs-lookup"><span data-stu-id="545ad-106">Gets the font that the date and time picker (DTP) control's child month calendar control is currently using.</span></span> <span data-ttu-id="545ad-107">Sie können diese Nachricht explizit senden oder das " [**DateTime \_ getmonthcalfont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) "-Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="545ad-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="545ad-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="545ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="545ad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="545ad-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="545ad-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="545ad-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="545ad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="545ad-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="545ad-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="545ad-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="545ad-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="545ad-113">Return value</span></span>

<span data-ttu-id="545ad-114">Gibt einen hFont-Wert zurück, der das Handle der aktuellen Schriftart ist.</span><span class="sxs-lookup"><span data-stu-id="545ad-114">Returns an HFONT value that is the handle to the current font.</span></span>

## <a name="requirements"></a><span data-ttu-id="545ad-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="545ad-115">Requirements</span></span>



| <span data-ttu-id="545ad-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="545ad-116">Requirement</span></span> | <span data-ttu-id="545ad-117">Wert</span><span class="sxs-lookup"><span data-stu-id="545ad-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="545ad-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="545ad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="545ad-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="545ad-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="545ad-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="545ad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="545ad-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="545ad-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="545ad-122">Header</span><span class="sxs-lookup"><span data-stu-id="545ad-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="545ad-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="545ad-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





