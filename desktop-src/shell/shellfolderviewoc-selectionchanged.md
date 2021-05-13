---
description: Gibt an, dass sich der Auswahlzustand eines oder mehrerer Elemente in der Ansicht geändert hat.
title: ShellFolderViewOC.SelectionChanged-Ereignis (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 85c37f4e-229f-4383-8218-10f8c2b0b8a0
ms.openlocfilehash: 53d6fc3eb6f13d136af603a3129ba75a46c3c6a6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841041"
---
# <a name="shellfolderviewocselectionchanged-event"></a><span data-ttu-id="07671-103">ShellFolderViewOC.SelectionChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="07671-103">ShellFolderViewOC.SelectionChanged event</span></span>

<span data-ttu-id="07671-104">Gibt an, dass sich der Auswahlzustand eines oder mehrerer Elemente in der Ansicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="07671-104">Indicates that the selection state of one or more items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="07671-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07671-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="07671-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="07671-106">Parameters</span></span>

<span data-ttu-id="07671-107">Dieser Ereignishandler verfügt über keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="07671-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="07671-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="07671-108">Remarks</span></span>

<span data-ttu-id="07671-109">Geben Sie wie hier gezeigt Ereignisbehandlungscode für dieses Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="07671-109">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="07671-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07671-110">Requirements</span></span>



| <span data-ttu-id="07671-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07671-111">Requirement</span></span> | <span data-ttu-id="07671-112">Wert</span><span class="sxs-lookup"><span data-stu-id="07671-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07671-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07671-113">Minimum supported client</span></span><br/> | <span data-ttu-id="07671-114">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07671-114">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07671-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07671-115">Minimum supported server</span></span><br/> | <span data-ttu-id="07671-116">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07671-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="07671-117">Header</span><span class="sxs-lookup"><span data-stu-id="07671-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="07671-118"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="07671-118"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="07671-119">Idl</span><span class="sxs-lookup"><span data-stu-id="07671-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="07671-120"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="07671-120"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="07671-121">DLL</span><span class="sxs-lookup"><span data-stu-id="07671-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07671-122"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="07671-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07671-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07671-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07671-124">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="07671-124">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




