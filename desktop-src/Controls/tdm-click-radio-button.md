---
title: TDM_CLICK_RADIO_BUTTON Meldung (kommstrg. h)
description: Simuliert die Aktion eines Options Felds in einem Aufgaben Dialogfeld.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- Windows-Steuerelemente für TDM_CLICK_RADIO_BUTTON Meldung
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76d465b1b937359a3d312a401914d497f9c9b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957099"
---
# <a name="tdm_click_radio_button-message"></a><span data-ttu-id="ae56f-104">TDM-Click-Optionsfeld \_ \_ \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="ae56f-104">TDM\_CLICK\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="ae56f-105">Simuliert die Aktion eines Options Felds in einem Aufgaben Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="ae56f-105">Simulates the action of a radio button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae56f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae56f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae56f-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae56f-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae56f-108">Ein **int** -Wert, der die ID des Options Felds angibt, auf das geklickt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae56f-108">An **int** value that specifies the ID of the radio button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="ae56f-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae56f-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae56f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="ae56f-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae56f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae56f-111">Return value</span></span>

<span data-ttu-id="ae56f-112">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ae56f-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae56f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae56f-113">Remarks</span></span>

<span data-ttu-id="ae56f-114">Die angegebene Optionsfeld-ID wird an die [**taskdialogcallbackproc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) -Rückruffunktion als Teil eines von [TDN \_ \_ \_ angeklickten](tdn-radio-button-clicked.md) Benachrichtigungs Codes gesendet.</span><span class="sxs-lookup"><span data-stu-id="ae56f-114">The specified radio button ID is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_RADIO\_BUTTON\_CLICKED](tdn-radio-button-clicked.md) notification code.</span></span> <span data-ttu-id="ae56f-115">Nachdem die Rückruffunktion zurückgegeben wurde, wird das Optionsfeld ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ae56f-115">After the callback function returns, the radio button will be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae56f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae56f-116">Requirements</span></span>



| <span data-ttu-id="ae56f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae56f-117">Requirement</span></span> | <span data-ttu-id="ae56f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ae56f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae56f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae56f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae56f-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae56f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae56f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae56f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae56f-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae56f-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae56f-123">Header</span><span class="sxs-lookup"><span data-stu-id="ae56f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae56f-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae56f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

