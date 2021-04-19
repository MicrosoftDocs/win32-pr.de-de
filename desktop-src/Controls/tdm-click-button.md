---
title: TDM_CLICK_BUTTON Meldung (kommstrg. h)
description: Simuliert die Aktion eines Schaltflächen-Click in einem Aufgaben Dialogfeld.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- Windows-Steuerelemente für TDM_CLICK_BUTTON Meldung
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345294"
---
# <a name="tdm_click_button-message"></a><span data-ttu-id="75014-104">TDM- \_ Click- \_ Schaltflächen Meldung</span><span class="sxs-lookup"><span data-stu-id="75014-104">TDM\_CLICK\_BUTTON message</span></span>

<span data-ttu-id="75014-105">Simuliert die Aktion eines Schaltflächen-Click in einem Aufgaben Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="75014-105">Simulates the action of a button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="75014-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75014-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75014-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75014-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75014-108">Ein **int** -Wert, der die ID der Schaltfläche angibt, auf die geklickt werden soll.</span><span class="sxs-lookup"><span data-stu-id="75014-108">An **int** that specifies the ID of the button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="75014-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75014-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75014-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="75014-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75014-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75014-111">Return value</span></span>

<span data-ttu-id="75014-112">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="75014-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="75014-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75014-113">Remarks</span></span>

<span data-ttu-id="75014-114">Die von *wParam* angegebene Schaltflächen-ID wird als Teil eines Benachrichtigungs Codes auf [TDN- \_ Schaltfläche \_](tdn-button-clicked.md) an die [**taskdialogcallbackproc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) -Rückruffunktion gesendet.</span><span class="sxs-lookup"><span data-stu-id="75014-114">The button ID specified by *wParam* is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) notification code.</span></span> <span data-ttu-id="75014-115">Nachdem die Rückruffunktion zurückgegeben wurde, wird das Aufgaben Dialogfeld geschlossen, wenn S \_ OK von der Rückruffunktion zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="75014-115">After the callback function returns, the task dialog is closed if S\_OK was returned from the callback function.</span></span> <span data-ttu-id="75014-116">Wenn ' \_ false ' von der Rückruffunktion zurückgegeben wurde, bleibt das Aufgaben Dialogfeld aktiv.</span><span class="sxs-lookup"><span data-stu-id="75014-116">If S\_FALSE was returned from the callback function, the task dialog remains active.</span></span>

## <a name="requirements"></a><span data-ttu-id="75014-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75014-117">Requirements</span></span>



| <span data-ttu-id="75014-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75014-118">Requirement</span></span> | <span data-ttu-id="75014-119">Wert</span><span class="sxs-lookup"><span data-stu-id="75014-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75014-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75014-120">Minimum supported client</span></span><br/> | <span data-ttu-id="75014-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75014-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75014-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75014-122">Minimum supported server</span></span><br/> | <span data-ttu-id="75014-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75014-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75014-124">Header</span><span class="sxs-lookup"><span data-stu-id="75014-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="75014-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="75014-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

