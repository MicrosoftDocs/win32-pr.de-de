---
title: NM_NCHITTEST Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn das Steuerelement eine WM- \_ nchittest-Nachricht empfängt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- Windows-Steuerelemente für NM_NCHITTEST Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8af39fd792ecb9aeb463957f49f5722737e6ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338737"
---
# <a name="nm_nchittest-notification-code"></a><span data-ttu-id="cadbe-105">NM \_ nchittest-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="cadbe-105">NM\_NCHITTEST notification code</span></span>

<span data-ttu-id="cadbe-106">Wird von einem Grund leisten-Steuerelement gesendet, wenn das Steuerelement eine [**WM- \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) -Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="cadbe-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="cadbe-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="cadbe-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cadbe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cadbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cadbe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cadbe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cadbe-110">Ein Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="cadbe-110">A pointer to a [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="cadbe-111">Der *PT* -Member enthält die Maus Koordinaten der Treffer Testnachricht.</span><span class="sxs-lookup"><span data-stu-id="cadbe-111">The *pt* member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cadbe-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cadbe-112">Return value</span></span>

<span data-ttu-id="cadbe-113">Sofern nicht anders angegeben, wird NULL zurückgegeben, damit das Steuerelement die Standard Verarbeitung der Treffer Testnachricht ausführen kann, oder einen der HT-Werte zurückgeben, der \* unter [**WM \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) dokumentiert ist, um die standardmäßige Treffer Testverarbeitung zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="cadbe-113">Unless otherwise specified, return zero to allow the control to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="cadbe-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cadbe-114">Requirements</span></span>



| <span data-ttu-id="cadbe-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cadbe-115">Requirement</span></span> | <span data-ttu-id="cadbe-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cadbe-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cadbe-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cadbe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cadbe-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cadbe-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cadbe-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cadbe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cadbe-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cadbe-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cadbe-121">Header</span><span class="sxs-lookup"><span data-stu-id="cadbe-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cadbe-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cadbe-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

