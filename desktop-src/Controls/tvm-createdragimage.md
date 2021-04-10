---
title: TVM_CREATEDRAGIMAGE Meldung (kommstrg. h)
description: Erstellt eine Zieh Bitmap für das angegebene Element in einem Strukturansicht-Steuerelement.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- Windows-Steuerelemente für TVM_CREATEDRAGIMAGE Meldung
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103904"
---
# <a name="tvm_createdragimage-message"></a><span data-ttu-id="acafa-104">TVM- \_ Meldung "fiatedragimage"</span><span class="sxs-lookup"><span data-stu-id="acafa-104">TVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="acafa-105">Erstellt eine Zieh Bitmap für das angegebene Element in einem Strukturansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="acafa-105">Creates a dragging bitmap for the specified item in a tree-view control.</span></span> <span data-ttu-id="acafa-106">Die Meldung erstellt außerdem eine Bildliste für die Bitmap und fügt der Bildliste die Bitmap hinzu.</span><span class="sxs-lookup"><span data-stu-id="acafa-106">The message also creates an image list for the bitmap and adds the bitmap to the image list.</span></span> <span data-ttu-id="acafa-107">Eine Anwendung kann das Bild anzeigen, wenn Sie das Element mithilfe der ImageList-Funktionen ziehen.</span><span class="sxs-lookup"><span data-stu-id="acafa-107">An application can display the image when dragging the item by using the image list functions.</span></span> <span data-ttu-id="acafa-108">Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Makros " \_ kreeview**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) " senden.</span><span class="sxs-lookup"><span data-stu-id="acafa-108">You can send this message explicitly or by using the [**TreeView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="acafa-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="acafa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acafa-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="acafa-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="acafa-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="acafa-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="acafa-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="acafa-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="acafa-113">Handle für das Element, das die neue Zieh Bitmap empfängt.</span><span class="sxs-lookup"><span data-stu-id="acafa-113">Handle to the item that receives the new dragging bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acafa-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="acafa-114">Return value</span></span>

<span data-ttu-id="acafa-115">Gibt das Handle für die Bildliste zurück, der die Zieh Bitmap hinzugefügt wurde, wenn erfolgreich, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="acafa-115">Returns the handle to the image list to which the dragging bitmap was added if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="acafa-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="acafa-116">Remarks</span></span>

<span data-ttu-id="acafa-117">Wenn Sie ein Strukturansicht-Steuerelement ohne zugeordnete Bildliste erstellen, können Sie das Bild, das während eines Zieh Vorgangs angezeigt wird, nicht mithilfe der TVM-Meldung " **\_ fiatedragimage** " erstellen.</span><span class="sxs-lookup"><span data-stu-id="acafa-117">If you create a tree-view control without an associated image list, you cannot use the **TVM\_CREATEDRAGIMAGE** message to create the image to display during a drag operation.</span></span> <span data-ttu-id="acafa-118">Sie müssen eine eigene Methode zum Erstellen eines Zieh Cursors implementieren.</span><span class="sxs-lookup"><span data-stu-id="acafa-118">You must implement your own method of creating a drag cursor.</span></span>

<span data-ttu-id="acafa-119">Die Anwendung ist dafür verantwortlich, die Bildliste zu zerstören, wenn Sie nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="acafa-119">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="acafa-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acafa-120">Requirements</span></span>



| <span data-ttu-id="acafa-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acafa-121">Requirement</span></span> | <span data-ttu-id="acafa-122">Wert</span><span class="sxs-lookup"><span data-stu-id="acafa-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="acafa-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="acafa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="acafa-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acafa-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="acafa-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="acafa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="acafa-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="acafa-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="acafa-127">Header</span><span class="sxs-lookup"><span data-stu-id="acafa-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="acafa-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="acafa-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





