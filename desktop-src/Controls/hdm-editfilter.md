---
title: HDM_EDITFILTER Meldung (kommstrg. h)
description: Verschiebt den Eingabefokus in das Bearbeitungsfeld, wenn eine Filter Schaltfläche den Fokus besitzt.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- Windows-Steuerelemente für HDM_EDITFILTER Meldung
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733c79bf747d3b55aa8dd38eb8fad8fdc83601e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742281"
---
# <a name="hdm_editfilter-message"></a><span data-ttu-id="8c71c-104">HDM- \_ EditFilter-Meldung</span><span class="sxs-lookup"><span data-stu-id="8c71c-104">HDM\_EDITFILTER message</span></span>

<span data-ttu-id="8c71c-105">Verschiebt den Eingabefokus in das Bearbeitungsfeld, wenn eine Filter Schaltfläche den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="8c71c-105">Moves the input focus to the edit box when a filter button has the focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c71c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c71c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c71c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c71c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c71c-108">Ein-Wert, der die zu bearbeitende Spalte angibt.</span><span class="sxs-lookup"><span data-stu-id="8c71c-108">A value specifying the column to edit.</span></span>

</dd> <dt>

<span data-ttu-id="8c71c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c71c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c71c-110">Ein Flag, das angibt, wie die Bearbeitungs Änderungen des Benutzers behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="8c71c-110">A flag that specifies how to handle the user's editing changes.</span></span> <span data-ttu-id="8c71c-111">Verwenden Sie dieses Flag, um anzugeben, was geschehen soll, wenn der Benutzer den Filter bearbeitet, wenn die Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c71c-111">Use this flag to specify what to do if the user is in the process of editing the filter when the message is sent.</span></span>



| <span data-ttu-id="8c71c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="8c71c-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="8c71c-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8c71c-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="8c71c-114"><dt></dt><dt> **True**</dt></span><span class="sxs-lookup"><span data-stu-id="8c71c-114"><dt></dt> <dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="8c71c-115">Verwerfen Sie die vom Benutzer vorgenommenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="8c71c-115">Discard the changes made by the user.</span></span> <br/> |
| <dl> <span data-ttu-id="8c71c-116"><dt></dt><dt> **False**</dt></span><span class="sxs-lookup"><span data-stu-id="8c71c-116"><dt></dt> <dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="8c71c-117">Akzeptieren Sie die vom Benutzer vorgenommenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="8c71c-117">Accept the changes made by the user.</span></span> <br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c71c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c71c-118">Return value</span></span>

<span data-ttu-id="8c71c-119">Gibt eine ganze Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="8c71c-119">Returns an integer.</span></span> <span data-ttu-id="8c71c-120">Das **LRESULT** wird in eine ganze Zahl umgewandelt, die **true**(1) oder **false**(0) angibt.</span><span class="sxs-lookup"><span data-stu-id="8c71c-120">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c71c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c71c-121">Requirements</span></span>



| <span data-ttu-id="8c71c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c71c-122">Requirement</span></span> | <span data-ttu-id="8c71c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="8c71c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c71c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c71c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8c71c-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c71c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c71c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c71c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8c71c-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c71c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c71c-128">Header</span><span class="sxs-lookup"><span data-stu-id="8c71c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c71c-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c71c-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c71c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c71c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c71c-131">**HDM- \_ ClearFilter**</span><span class="sxs-lookup"><span data-stu-id="8c71c-131">**HDM\_CLEARFILTER**</span></span>](hdm-clearfilter.md)
</dt> </dl>

 

 





