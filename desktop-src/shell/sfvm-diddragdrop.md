---
description: Sfvm \_ diddragdrop kann geändert oder nicht verfügbar sein.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: SFVM_DIDDRAGDROP Meldung (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994918"
---
# <a name="sfvm_diddragdrop-message"></a><span data-ttu-id="b495e-103">Sfvm- \_ diddragdrop-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b495e-103">SFVM\_DIDDRAGDROP message</span></span>

<span data-ttu-id="b495e-104">\[**Sfvm \_ Diddragdrop** steht zur Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b495e-104">\[**SFVM\_DIDDRAGDROP** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b495e-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b495e-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="b495e-106">Benachrichtigt die Rückruffunktion, dass ein Drag & Drop-Vorgang begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="b495e-106">Notifies the callback function that a drag-and-drop operation has begun.</span></span> <span data-ttu-id="b495e-107">Wird von [**ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)verwendet.</span><span class="sxs-lookup"><span data-stu-id="b495e-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a><span data-ttu-id="b495e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b495e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b495e-109">*dweffect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b495e-109">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b495e-110">Ein Drop Effect-Spezifizierer aus der [**dropffect**](../com/dropeffect-constants.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="b495e-110">A drop effect specifier from the [**DROPEFFECT**](../com/dropeffect-constants.md) enumeration.</span></span> <span data-ttu-id="b495e-111">Dies wird durch Aufrufen von [**shdodragdrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop)erreicht.</span><span class="sxs-lookup"><span data-stu-id="b495e-111">This is obtained by calling [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span></span>

</dd> <dt>

<span data-ttu-id="b495e-112">*Pido* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b495e-112">*pIdo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b495e-113">Ein Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Instanz.</span><span class="sxs-lookup"><span data-stu-id="b495e-113">A pointer to the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b495e-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b495e-114">Requirements</span></span>



| <span data-ttu-id="b495e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b495e-115">Requirement</span></span> | <span data-ttu-id="b495e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b495e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b495e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b495e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b495e-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b495e-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b495e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b495e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b495e-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b495e-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b495e-121">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b495e-121">End of client support</span></span><br/>    | <span data-ttu-id="b495e-122">Windows XP mit SP2</span><span class="sxs-lookup"><span data-stu-id="b495e-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="b495e-123">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b495e-123">End of server support</span></span><br/>    | <span data-ttu-id="b495e-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b495e-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="b495e-125">Header</span><span class="sxs-lookup"><span data-stu-id="b495e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b495e-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="b495e-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
