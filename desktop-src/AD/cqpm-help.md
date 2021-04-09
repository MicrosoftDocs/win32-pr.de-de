---
title: CQPM_HELP Meldung (cmnquery. h)
description: Wird an die cqpageproc-Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, damit die Seiten Erweiterung die kontextbezogene Hilfe für die Seite anzeigen kann.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- CQPM_HELP Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7635b87a0ba489c63f87fb32742c37a9f7044860
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103066"
---
# <a name="cqpm_help-message"></a><span data-ttu-id="a740c-104">Cqpm- \_ Hilfe Meldung</span><span class="sxs-lookup"><span data-stu-id="a740c-104">CQPM\_HELP message</span></span>

<span data-ttu-id="a740c-105">Die **cqpm- \_ Hilfe** Nachricht wird an die [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, damit die Seiten Erweiterung die kontextbezogene Hilfe für die Seite anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="a740c-105">The **CQPM\_HELP** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to allow the page extension to display context-sensitive help for the page.</span></span> <span data-ttu-id="a740c-106">Wenn möglich, sollte die Abfrage Seiten Erweiterung eine kontextbezogene Hilfe als Reaktion auf dieses Ereignis anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a740c-106">If possible, the query page extension should display context-sensitive help in response to this event.</span></span>

## <a name="parameters"></a><span data-ttu-id="a740c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a740c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a740c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a740c-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a740c-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a740c-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a740c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a740c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a740c-111">Ein Zeiger auf eine [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur, die zusätzliche Daten über das Menü Element, das Steuerelement, das Dialogfeld oder das Fenster enthält, für das die kontextbezogene Hilfe angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="a740c-111">Pointer to a [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure that contains additional data about the menu item, control, dialog box, or window for which context-sensitive help is requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a740c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a740c-112">Return value</span></span>

<span data-ttu-id="a740c-113">Der Rückgabewert für diese Nachricht wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a740c-113">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a740c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a740c-114">Requirements</span></span>



| <span data-ttu-id="a740c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a740c-115">Requirement</span></span> | <span data-ttu-id="a740c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a740c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a740c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a740c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a740c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a740c-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="a740c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a740c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a740c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a740c-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="a740c-121">Header</span><span class="sxs-lookup"><span data-stu-id="a740c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a740c-122"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="a740c-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a740c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a740c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a740c-124">**Cqpageproc**</span><span class="sxs-lookup"><span data-stu-id="a740c-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="a740c-125">**HELPINFO**</span><span class="sxs-lookup"><span data-stu-id="a740c-125">**HELPINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

