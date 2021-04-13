---
title: EM_GETWORDWRAPMODE Meldung (RichEdit. h)
description: Ruft die aktuellen Zeilenumbruch-und Wort Umbruch Optionen für das Rich-Edit-Steuerelement ab.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- Windows-Steuerelemente für EM_GETWORDWRAPMODE Meldung
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475567"
---
# <a name="em_getwordwrapmode-message"></a><span data-ttu-id="df9e9-104">EM \_ getwordwrapmode-Meldung</span><span class="sxs-lookup"><span data-stu-id="df9e9-104">EM\_GETWORDWRAPMODE message</span></span>

<span data-ttu-id="df9e9-105">Ruft die aktuellen Zeilenumbruch-und Wort Umbruch Optionen für das Rich-Edit-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="df9e9-105">Gets the current word wrap and word-break options for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="df9e9-106">Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="df9e9-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="df9e9-107">Sie wird in höheren Versionen der Rich-Edit-Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="df9e9-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="df9e9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="df9e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df9e9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df9e9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df9e9-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="df9e9-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="df9e9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df9e9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df9e9-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="df9e9-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df9e9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df9e9-113">Return value</span></span>

<span data-ttu-id="df9e9-114">Die Meldung gibt die aktuellen Optionen für Zeilenumbruch und Wort Umbruch zurück.</span><span class="sxs-lookup"><span data-stu-id="df9e9-114">The message returns the current word wrap and word-break options.</span></span>

## <a name="remarks"></a><span data-ttu-id="df9e9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df9e9-115">Remarks</span></span>

<span data-ttu-id="df9e9-116">Diese Nachricht darf nicht von der Anwendungs definierten Prozedur für das Wort Umbruch gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="df9e9-116">This message must not be sent by the application-defined, word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="df9e9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df9e9-117">Requirements</span></span>



| <span data-ttu-id="df9e9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df9e9-118">Requirement</span></span> | <span data-ttu-id="df9e9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="df9e9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df9e9-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df9e9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="df9e9-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df9e9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="df9e9-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df9e9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="df9e9-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df9e9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df9e9-124">Header</span><span class="sxs-lookup"><span data-stu-id="df9e9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="df9e9-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="df9e9-125"><dt>Richedit.h</dt></span></span> </dl> |



 

 





