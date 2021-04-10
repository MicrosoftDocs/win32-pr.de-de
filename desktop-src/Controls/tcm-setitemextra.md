---
title: TCM_SETITEMEXTRA Meldung (kommstrg. h)
description: Legt die Anzahl von Bytes pro Registerkarte fest, die für Anwendungs definierte Daten in einem Registerkarten-Steuerelement reserviert ist. Sie können diese Nachricht explizit oder mithilfe des tabctrl-Elements tabctrl/ \_ titemextra senden.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- Windows-Steuerelemente für TCM_SETITEMEXTRA Meldung
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102855"
---
# <a name="tcm_setitemextra-message"></a><span data-ttu-id="da138-105">TCM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="da138-105">TCM\_SETITEMEXTRA message</span></span>

<span data-ttu-id="da138-106">Legt die Anzahl von Bytes pro Registerkarte fest, die für Anwendungs definierte Daten in einem Registerkarten-Steuerelement reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="da138-106">Sets the number of bytes per tab reserved for application-defined data in a tab control.</span></span> <span data-ttu-id="da138-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl-Elements tabctrl/ \_ titemextra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) senden.</span><span class="sxs-lookup"><span data-stu-id="da138-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="da138-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="da138-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da138-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da138-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da138-110">Anzahl zusätzlicher bytes.</span><span class="sxs-lookup"><span data-stu-id="da138-110">Number of extra bytes.</span></span>

</dd> <dt>

<span data-ttu-id="da138-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da138-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="da138-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="da138-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da138-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da138-113">Return value</span></span>

<span data-ttu-id="da138-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="da138-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="da138-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da138-115">Remarks</span></span>

<span data-ttu-id="da138-116">Standardmäßig beträgt die Anzahl zusätzlicher Bytes vier.</span><span class="sxs-lookup"><span data-stu-id="da138-116">By default, the number of extra bytes is four.</span></span> <span data-ttu-id="da138-117">Eine Anwendung, die die Anzahl zusätzlicher Bytes ändert, kann die [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur nicht zum Abrufen und Festlegen der Anwendungs definierten Daten für eine Registerkarte verwenden. Stattdessen müssen Sie eine neue Struktur definieren, die aus der [**tcitemheader**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) -Struktur gefolgt von Anwendungs definierten Membern besteht.</span><span class="sxs-lookup"><span data-stu-id="da138-117">An application that changes the number of extra bytes cannot use the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure to retrieve and set the application-defined data for a tab. Instead, you must define a new structure that consists of the [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) structure followed by application-defined members.</span></span>

<span data-ttu-id="da138-118">Eine Anwendung sollte nur die Anzahl zusätzlicher Bytes ändern, wenn ein Registerkarten-Steuerelement keine Registerkarten enthält.</span><span class="sxs-lookup"><span data-stu-id="da138-118">An application should only change the number of extra bytes when a tab control does not contain any tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="da138-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da138-119">Requirements</span></span>



| <span data-ttu-id="da138-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da138-120">Requirement</span></span> | <span data-ttu-id="da138-121">Wert</span><span class="sxs-lookup"><span data-stu-id="da138-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da138-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da138-122">Minimum supported client</span></span><br/> | <span data-ttu-id="da138-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da138-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da138-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da138-124">Minimum supported server</span></span><br/> | <span data-ttu-id="da138-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da138-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da138-126">Header</span><span class="sxs-lookup"><span data-stu-id="da138-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="da138-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="da138-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





