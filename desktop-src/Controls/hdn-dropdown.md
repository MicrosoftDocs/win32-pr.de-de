---
title: HDN_DROPDOWN Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Header Steuerelement an das übergeordnete Element gesendet, wenn auf den Dropdown Pfeil im Header Steuerelement geklickt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- Windows-Steuerelemente für HDN_DROPDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859352"
---
# <a name="hdn_dropdown-notification-code"></a><span data-ttu-id="de203-105">Benachrichtigungs Code für Hdn- \_ Dropdown</span><span class="sxs-lookup"><span data-stu-id="de203-105">HDN\_DROPDOWN notification code</span></span>

<span data-ttu-id="de203-106">Wird von einem Header Steuerelement an das übergeordnete Element gesendet, wenn auf den Dropdown Pfeil im Header Steuerelement geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="de203-106">Sent by a header control to its parent when the drop-down arrow on the header control is clicked.</span></span> <span data-ttu-id="de203-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="de203-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="de203-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de203-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de203-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de203-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de203-110">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="de203-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information on the header control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de203-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de203-111">Return value</span></span>

<span data-ttu-id="de203-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="de203-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de203-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de203-113">Remarks</span></span>

<span data-ttu-id="de203-114">Das Beispiel im Abschnitt Syntax zeigt, wie der Benachrichtigungs Empfänger **LPARAM** zum Abrufen der [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur umwirft.</span><span class="sxs-lookup"><span data-stu-id="de203-114">The example in the Syntax section shows how the notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="de203-115">**WParam** enthält die ID des Steuer Elements, das diese Nachricht sendet.</span><span class="sxs-lookup"><span data-stu-id="de203-115">**WPARAM** contains the ID of the control that sends this message.</span></span>

<span data-ttu-id="de203-116">Diese Meldung wird nur gesendet, wenn \_ für das Header Element Style HDF SplitButton festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="de203-116">This message is sent only if style HDF\_SPLITBUTTON is set on the header item.</span></span>

## <a name="requirements"></a><span data-ttu-id="de203-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de203-117">Requirements</span></span>



| <span data-ttu-id="de203-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de203-118">Requirement</span></span> | <span data-ttu-id="de203-119">Wert</span><span class="sxs-lookup"><span data-stu-id="de203-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de203-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de203-120">Minimum supported client</span></span><br/> | <span data-ttu-id="de203-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de203-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de203-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de203-122">Minimum supported server</span></span><br/> | <span data-ttu-id="de203-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de203-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de203-124">Header</span><span class="sxs-lookup"><span data-stu-id="de203-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="de203-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="de203-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





