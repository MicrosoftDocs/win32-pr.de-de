---
description: Ruft ein folderitems-Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.
title: Shellfolderview. SelectedItems-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectedItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1ee3bf2e-f9c9-47d9-a0f2-efedd69770c5
ms.openlocfilehash: c6ade3a6e25d5de6bfa1661207473dac72ace2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994999"
---
# <a name="shellfolderviewselecteditems-method"></a><span data-ttu-id="d1d0f-103">Shellfolderview. SelectedItems-Methode</span><span class="sxs-lookup"><span data-stu-id="d1d0f-103">ShellFolderView.SelectedItems method</span></span>

<span data-ttu-id="d1d0f-104">Ruft ein [**folderitems**](folderitems.md) -Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="d1d0f-104">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d0f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1d0f-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="d1d0f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1d0f-106">Parameters</span></span>

<span data-ttu-id="d1d0f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d1d0f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1d0f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1d0f-108">Return value</span></span>

<span data-ttu-id="d1d0f-109">Type: **[ **folderitems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d1d0f-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="d1d0f-110">Ein Objekt Verweis auf das [**folderitems**](folderitems.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d1d0f-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1d0f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1d0f-111">Remarks</span></span>

<span data-ttu-id="d1d0f-112">**SelectedItems** kann nur auf dem lokalen System aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d1d0f-112">**SelectedItems** can only be called on the local system.</span></span> <span data-ttu-id="d1d0f-113">Es funktioniert nicht, wenn es auf einer Webseite über HTTP oder UNC ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1d0f-113">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="d1d0f-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1d0f-114">Examples</span></span>

<span data-ttu-id="d1d0f-115">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode in JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="d1d0f-115">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectedItemsJ()
    {
        var objFolderItems;
        
        objFolderItems = WebOC.Document.SelectedItems();
        if (objFolderItems != null)
        {
            alert("Got FolderItems object.");
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
<INPUT id=SelectedItems 
       type=button 
       value=SelectedItems 
       name=SelectedItems 
       onclick="fnShellFolderViewSelectedItemsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="d1d0f-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d1d0f-116">Requirements</span></span>



| <span data-ttu-id="d1d0f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1d0f-117">Requirement</span></span> | <span data-ttu-id="d1d0f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d1d0f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d0f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1d0f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d0f-120">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1d0f-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d1d0f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1d0f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d0f-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1d0f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d1d0f-123">Header</span><span class="sxs-lookup"><span data-stu-id="d1d0f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1d0f-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1d0f-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d1d0f-125">IDL</span><span class="sxs-lookup"><span data-stu-id="d1d0f-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1d0f-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1d0f-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d1d0f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d1d0f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1d0f-128"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d0f-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




