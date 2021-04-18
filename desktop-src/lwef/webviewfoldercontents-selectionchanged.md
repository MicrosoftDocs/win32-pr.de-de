---
title: Webviewfoldercontents. SelectionChanged-Ereignis (Shldisp. h)
description: Tritt auf, wenn sich der Auswahl Zustand eines Elements oder der Elemente in der Ansicht geändert hat.
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- SelectionChanged-Ereignis Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- SelectionChanged
api_location:
- Shell32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8421e9d06ff9fd24256da8a23cdd100b5749968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518749"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a><span data-ttu-id="132e3-104">Webviewfoldercontents. SelectionChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="132e3-104">WebViewFolderContents.SelectionChanged event</span></span>

<span data-ttu-id="132e3-105">Tritt auf, wenn sich der Auswahl Zustand eines Elements oder der Elemente in der Ansicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="132e3-105">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="132e3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="132e3-106">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="132e3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="132e3-107">Parameters</span></span>

<span data-ttu-id="132e3-108">Dieser Ereignishandler verfügt über keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="132e3-108">This event handler has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="132e3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="132e3-109">Examples</span></span>

<span data-ttu-id="132e3-110">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieses Ereignisses für JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="132e3-110">The following example shows the proper usage of this event for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectionChangedJ()
    {
        alert("SelectionChanged event was called");
    }
</script>

<script language="JavaScript" for="FileList" event="SelectionChanged">
    fnWebViewFolderContentsSelectionChangedJ();
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="132e3-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="132e3-111">Requirements</span></span>



| <span data-ttu-id="132e3-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="132e3-112">Requirement</span></span> | <span data-ttu-id="132e3-113">Wert</span><span class="sxs-lookup"><span data-stu-id="132e3-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="132e3-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="132e3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="132e3-115">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="132e3-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="132e3-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="132e3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="132e3-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="132e3-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="132e3-118">Header</span><span class="sxs-lookup"><span data-stu-id="132e3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="132e3-119"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="132e3-119"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="132e3-120">IDL</span><span class="sxs-lookup"><span data-stu-id="132e3-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="132e3-121"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="132e3-121"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="132e3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="132e3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="132e3-123"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="132e3-123"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





