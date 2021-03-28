---
description: 'Benachrichtigt das Rückruf Objekt, dass einer seiner Symbolleisten-oder Menübefehle vom Benutzer aufgerufen wurde. Wird von ishellfolderviewcb:: messagesfvcb verwendet.'
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: SFVM_INVOKECOMMAND Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868695"
---
# <a name="sfvm_invokecommand-message"></a><span data-ttu-id="c2588-104">Sfvm \_ InvokeCommand-Meldung</span><span class="sxs-lookup"><span data-stu-id="c2588-104">SFVM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="c2588-105">Benachrichtigt das Rückruf Objekt, dass einer seiner Symbolleisten-oder Menübefehle vom Benutzer aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c2588-105">Notifies the callback object that one of its toolbar or menu commands has been invoked by the user.</span></span> <span data-ttu-id="c2588-106">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2588-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a><span data-ttu-id="c2588-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2588-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2588-108">*idcmd* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2588-108">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2588-109">Die Befehls-ID der ausgewählten Symbolleiste oder des ausgewählten Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="c2588-109">The command ID of the selected toolbar or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2588-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2588-110">Remarks</span></span>

<span data-ttu-id="c2588-111">Diese Meldung dient im wesentlichen derselben Funktion wie eine [**WM- \_ Befehls**](../menurc/wm-command.md) Nachricht in einer herkömmlichen Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="c2588-111">This message serves essentially the same function as a [**WM\_COMMAND**](../menurc/wm-command.md) message in a conventional window procedure.</span></span> <span data-ttu-id="c2588-112">Dadurch kann das Rückruf Objekt alle Elemente verarbeiten, die es dem Windows-Explorer-Tool oder der Menüleiste hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="c2588-112">It allows the callback object to handle any items that it has added to the Windows Explorer tool or menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2588-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c2588-113">Requirements</span></span>



| <span data-ttu-id="c2588-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2588-114">Requirement</span></span> | <span data-ttu-id="c2588-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c2588-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c2588-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2588-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c2588-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2588-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c2588-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2588-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c2588-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2588-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c2588-120">Header</span><span class="sxs-lookup"><span data-stu-id="c2588-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2588-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2588-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
