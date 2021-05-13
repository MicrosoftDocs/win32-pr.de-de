---
description: 'ShellFolderView.SelectionChanged-Ereignis: Tritt auf, wenn sich der Auswahlzustand eines Elements oder eines Elements in der Ansicht geändert hat.'
title: ShellFolderView.SelectionChanged-Ereignis (Shldisp.h)
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
ms.assetid: e91b72fd-fd26-4e38-8e80-41febec3ca03
ms.openlocfilehash: f029ffb217249909e966b592280abf38b2ba2edd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842571"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="a7071-103">ShellFolderView.SelectionChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a7071-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="a7071-104">Tritt ein, wenn sich der Auswahlzustand eines Elements oder eines Elements in der Ansicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a7071-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7071-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7071-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="a7071-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7071-106">Parameters</span></span>

<span data-ttu-id="a7071-107">Dieser Ereignishandler verfügt über keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a7071-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7071-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7071-108">Requirements</span></span>



| <span data-ttu-id="a7071-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7071-109">Requirement</span></span> | <span data-ttu-id="a7071-110">Wert</span><span class="sxs-lookup"><span data-stu-id="a7071-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7071-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7071-111">Minimum supported client</span></span><br/> | <span data-ttu-id="a7071-112">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7071-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a7071-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7071-113">Minimum supported server</span></span><br/> | <span data-ttu-id="a7071-114">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7071-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a7071-115">Header</span><span class="sxs-lookup"><span data-stu-id="a7071-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7071-116"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a7071-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a7071-117">Idl</span><span class="sxs-lookup"><span data-stu-id="a7071-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7071-118"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7071-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a7071-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a7071-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7071-120"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a7071-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




