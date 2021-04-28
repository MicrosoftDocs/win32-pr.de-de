---
title: WebViewFolderContents.SelectionChanged-Ereignis (Shldisp.h)
description: 'WebViewFolderContents.SelectionChanged-Ereignis: Tritt auf, wenn sich der Auswahlzustand eines Elements oder elements in der Ansicht geändert hat.'
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- SelectionChanged-Ereignis Legacy-Windows-Umgebungsfeatures
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
ms.openlocfilehash: ea6176cb2a1703d48cd2ddec8069c65d7efc978f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102658"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a><span data-ttu-id="b631d-104">WebViewFolderContents.SelectionChanged-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b631d-104">WebViewFolderContents.SelectionChanged event</span></span>

<span data-ttu-id="b631d-105">Tritt ein, wenn sich der Auswahlzustand eines Elements oder elements in der Ansicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="b631d-105">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b631d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b631d-106">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="b631d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b631d-107">Parameters</span></span>

<span data-ttu-id="b631d-108">Dieser Ereignishandler verfügt über keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b631d-108">This event handler has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="b631d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b631d-109">Examples</span></span>

<span data-ttu-id="b631d-110">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieses Ereignisses für JScript, das in HTML eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="b631d-110">The following example shows the proper usage of this event for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b631d-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b631d-111">Requirements</span></span>



| <span data-ttu-id="b631d-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b631d-112">Requirement</span></span> | <span data-ttu-id="b631d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b631d-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b631d-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b631d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b631d-115">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b631d-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b631d-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b631d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b631d-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b631d-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b631d-118">Header</span><span class="sxs-lookup"><span data-stu-id="b631d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b631d-119"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b631d-119"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b631d-120">Idl</span><span class="sxs-lookup"><span data-stu-id="b631d-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b631d-121"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="b631d-121"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b631d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b631d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b631d-123"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b631d-123"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





