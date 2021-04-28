---
description: 'ShellFolderView.FocusedItem-Eigenschaft: Ruft ein FolderItem-Objekt ab, das das Element mit dem Eingabefokus darstellt.'
ms.assetid: ca88801d-c8fa-4c1c-9294-f52eada40ff6
title: ShellFolderView.FocusedItem-Eigenschaft (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.FocusedItem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4f661f555f1492a3323fa3749a8dffd6f00f411d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104008"
---
# <a name="shellfolderviewfocuseditem-property"></a><span data-ttu-id="26a44-103">ShellFolderView.FocusedItem (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="26a44-103">ShellFolderView.FocusedItem property</span></span>

<span data-ttu-id="26a44-104">Ruft ein [**FolderItem-Objekt**](folderitem.md) ab, das das Element mit dem Eingabefokus darstellt.</span><span class="sxs-lookup"><span data-stu-id="26a44-104">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="26a44-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="26a44-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="26a44-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="26a44-106">Syntax</span></span>


```JScript
objFocusedItem = ShellFolderView.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="26a44-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="26a44-107">Property value</span></span>

<span data-ttu-id="26a44-108">Eine Variable vom Typ [**IDispatch,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) die das fokussierte Elementobjekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="26a44-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="remarks"></a><span data-ttu-id="26a44-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26a44-109">Remarks</span></span>

<span data-ttu-id="26a44-110">**FocusedItem** kann nur auf dem lokalen System aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="26a44-110">**FocusedItem** can only be called on the local system.</span></span> <span data-ttu-id="26a44-111">Sie funktioniert nicht, wenn sie auf einer Webseite über HTTP oder UNC ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26a44-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="26a44-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26a44-112">Examples</span></span>

<span data-ttu-id="26a44-113">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode in JScript, eingebettet in HTML.</span><span class="sxs-lookup"><span data-stu-id="26a44-113">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFocusedItemJ()
    {
        var objFolderItem;
        
        objFolderItem = WebOC.Document.FocusedItem;
        if (objFolderItem != null)
        {
            alert("Got FolderItem object.");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=FocusedItem 
       type=button 
       value=FocusedItem 
       name=FocusedItem 
       onclick="fnShellFolderViewFocusedItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="26a44-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26a44-114">Requirements</span></span>



| <span data-ttu-id="26a44-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26a44-115">Requirement</span></span> | <span data-ttu-id="26a44-116">Wert</span><span class="sxs-lookup"><span data-stu-id="26a44-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26a44-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26a44-117">Minimum supported client</span></span><br/> | <span data-ttu-id="26a44-118">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26a44-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="26a44-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26a44-119">Minimum supported server</span></span><br/> | <span data-ttu-id="26a44-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26a44-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="26a44-121">Header</span><span class="sxs-lookup"><span data-stu-id="26a44-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="26a44-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="26a44-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="26a44-123">Idl</span><span class="sxs-lookup"><span data-stu-id="26a44-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26a44-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="26a44-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="26a44-125">DLL</span><span class="sxs-lookup"><span data-stu-id="26a44-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26a44-126"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="26a44-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
