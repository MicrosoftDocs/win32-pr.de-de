---
description: Wird an das Besitzer Fenster eines Steuer Elements oder Menü Elements gesendet, wenn das Steuerelement oder das Menü erstellt wird.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: DFM_WM_MEASUREITEM Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393437"
---
# <a name="dfm_wm_measureitem-message"></a><span data-ttu-id="439f1-103">DFM- \_ WM- \_ MeasureItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="439f1-103">DFM\_WM\_MEASUREITEM message</span></span>

<span data-ttu-id="439f1-104">Wird an das Besitzer Fenster eines Steuer Elements oder Menü Elements gesendet, wenn das Steuerelement oder das Menü erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="439f1-104">Sent to the owner window of a control or menu item when the control or menu is created.</span></span>


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a><span data-ttu-id="439f1-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="439f1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="439f1-106">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="439f1-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="439f1-107">Der Wert des **ctlid** -Members der [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, auf die durch den *lpmeasureitem* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="439f1-107">The value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter.</span></span> <span data-ttu-id="439f1-108">Dieser Wert identifiziert das Steuerelement, das die **DFM- \_ WM- \_ MeasureItem** -Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="439f1-108">This value identifies the control that sent the **DFM\_WM\_MEASUREITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="439f1-109">*lpmeasureitem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="439f1-109">*lpMeasureItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="439f1-110">Ein Zeiger auf eine [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, die die Dimensionen des vom Besitzer gezeichneten Steuer Elements oder Menü Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="439f1-110">A pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="439f1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="439f1-111">Remarks</span></span>

<span data-ttu-id="439f1-112">Wenn das Besitzer Fenster die **DFM- \_ WM- \_ MeasureItem** -Nachricht empfängt, füllt der Besitzer die [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur aus, auf die durch den *lpmeasureitem* -Parameter der Nachricht verwiesen wird, und gibt zurück. Dadurch wird das System über die Abmessungen des Steuer Elements informiert.</span><span class="sxs-lookup"><span data-stu-id="439f1-112">When the owner window receives the **DFM\_WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lpMeasureItem* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="439f1-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="439f1-113">Requirements</span></span>



| <span data-ttu-id="439f1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="439f1-114">Requirement</span></span> | <span data-ttu-id="439f1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="439f1-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="439f1-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="439f1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="439f1-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="439f1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="439f1-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="439f1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="439f1-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="439f1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="439f1-120">Header</span><span class="sxs-lookup"><span data-stu-id="439f1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="439f1-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="439f1-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
