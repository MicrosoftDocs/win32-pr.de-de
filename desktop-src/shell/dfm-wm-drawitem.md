---
description: Wird an das übergeordnete Fenster eines von einem Besitzer gezeichneten Steuer Elements oder Menüs gesendet, wenn sich ein visueller Aspekt des Steuer Elements oder Menüs geändert hat.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: DFM_WM_DRAWITEM Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977265"
---
# <a name="dfm_wm_drawitem-message"></a><span data-ttu-id="c93ac-103">DFM- \_ WM- \_ DrawItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c93ac-103">DFM\_WM\_DRAWITEM message</span></span>

<span data-ttu-id="c93ac-104">Wird an das übergeordnete Fenster eines von einem Besitzer gezeichneten Steuer Elements oder Menüs gesendet, wenn sich ein visueller Aspekt des Steuer Elements oder Menüs geändert hat.</span><span class="sxs-lookup"><span data-stu-id="c93ac-104">Sent to the parent window of an owner-drawn control or menu when a visual aspect of the control or menu has changed.</span></span>


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a><span data-ttu-id="c93ac-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c93ac-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c93ac-106">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c93ac-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c93ac-107">Der Bezeichner des Steuer Elements, das die **DFM- \_ WM- \_ DrawItem** -Nachricht gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="c93ac-107">The identifier of the control that sent the **DFM\_WM\_DRAWITEM** message.</span></span> <span data-ttu-id="c93ac-108">Wenn die Nachricht von einem Menü gesendet wurde, ist dieser Parameter gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c93ac-108">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="c93ac-109">*lpdrawitem* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c93ac-109">*lpDrawItem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c93ac-110">Ein Zeiger auf eine [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur, die Informationen über das zu zeichende Element und den Typ der erforderlichen Zeichnung enthält.</span><span class="sxs-lookup"><span data-stu-id="c93ac-110">A pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c93ac-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c93ac-111">Return value</span></span>

<span data-ttu-id="c93ac-112">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c93ac-112">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c93ac-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c93ac-113">Remarks</span></span>

<span data-ttu-id="c93ac-114">Der **itemaction** -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur gibt den Zeichnungs Vorgang an, den eine Anwendung ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="c93ac-114">The **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="c93ac-115">Vor der Rückgabe aus der Verarbeitung dieser Nachricht muss eine Anwendung sicherstellen, dass der vom **hdc** -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur identifizierte Gerätekontext den Standardstatus aufweist.</span><span class="sxs-lookup"><span data-stu-id="c93ac-115">Before returning from processing this message, an application should ensure that the device context identified by the **hDC** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="c93ac-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c93ac-116">Requirements</span></span>



| <span data-ttu-id="c93ac-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c93ac-117">Requirement</span></span> | <span data-ttu-id="c93ac-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c93ac-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c93ac-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c93ac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c93ac-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c93ac-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c93ac-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c93ac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c93ac-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c93ac-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c93ac-123">Header</span><span class="sxs-lookup"><span data-stu-id="c93ac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c93ac-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c93ac-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
