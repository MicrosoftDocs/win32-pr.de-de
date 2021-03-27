---
description: Gibt an, dass sich der Auswahl Zustand eines oder mehrerer Elemente in der Ansicht geändert hat.
title: Shellfolderviewoc. SelectionChanged-Ereignis (Shldisp. h)
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
ms.openlocfilehash: 3f88ad698b990847a9b7f2fa1b74cc5b53ec7beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347919"
---
# <a name="shellfolderviewocselectionchanged-event"></a><span data-ttu-id="9db0a-103">Shellfolderviewoc. SelectionChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9db0a-103">ShellFolderViewOC.SelectionChanged event</span></span>

<span data-ttu-id="9db0a-104">Gibt an, dass sich der Auswahl Zustand eines oder mehrerer Elemente in der Ansicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9db0a-104">Indicates that the selection state of one or more items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db0a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9db0a-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="9db0a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9db0a-106">Parameters</span></span>

<span data-ttu-id="9db0a-107">Dieser Ereignishandler verfügt über keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9db0a-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9db0a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9db0a-108">Remarks</span></span>

<span data-ttu-id="9db0a-109">Geben Sie den Ereignis Behandlungs Code für dieses Ereignis an, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9db0a-109">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="9db0a-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9db0a-110">Requirements</span></span>



| <span data-ttu-id="9db0a-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9db0a-111">Requirement</span></span> | <span data-ttu-id="9db0a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="9db0a-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db0a-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9db0a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9db0a-114">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9db0a-114">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9db0a-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9db0a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9db0a-116">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9db0a-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9db0a-117">Header</span><span class="sxs-lookup"><span data-stu-id="9db0a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9db0a-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9db0a-118"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9db0a-119">IDL</span><span class="sxs-lookup"><span data-stu-id="9db0a-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9db0a-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9db0a-120"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9db0a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9db0a-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9db0a-122"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="9db0a-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9db0a-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9db0a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db0a-124">**Shellfolderviewoc**</span><span class="sxs-lookup"><span data-stu-id="9db0a-124">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




