---
description: 'ShellFolderView.SelectedItems-Methode: Ruft ein FolderItems-Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.'
title: ShellFolderView.SelectedItems-Methode (Shldisp.h)
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
ms.openlocfilehash: 485eda530adc4955abb27899d67ac0900eb0a910
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840741"
---
# <a name="shellfolderviewselecteditems-method"></a><span data-ttu-id="31d61-103">ShellFolderView.SelectedItems-Methode</span><span class="sxs-lookup"><span data-stu-id="31d61-103">ShellFolderView.SelectedItems method</span></span>

<span data-ttu-id="31d61-104">Ruft ein [**FolderItems-Objekt**](folderitems.md) ab, das alle ausgewählten Elemente in der Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="31d61-104">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="31d61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31d61-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="31d61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31d61-106">Parameters</span></span>

<span data-ttu-id="31d61-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="31d61-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31d61-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31d61-108">Return value</span></span>

<span data-ttu-id="31d61-109">Typ: **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="31d61-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="31d61-110">Ein Objektverweis auf das [**FolderItems-Objekt.**](folderitems.md)</span><span class="sxs-lookup"><span data-stu-id="31d61-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="31d61-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31d61-111">Remarks</span></span>

<span data-ttu-id="31d61-112">**SelectedItems** kann nur auf dem lokalen System aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="31d61-112">**SelectedItems** can only be called on the local system.</span></span> <span data-ttu-id="31d61-113">Sie funktioniert nicht, wenn sie auf einer Webseite über HTTP oder UNC ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31d61-113">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="31d61-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31d61-114">Examples</span></span>

<span data-ttu-id="31d61-115">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode in JScript, eingebettet in HTML.</span><span class="sxs-lookup"><span data-stu-id="31d61-115">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="31d61-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31d61-116">Requirements</span></span>



| <span data-ttu-id="31d61-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31d61-117">Requirement</span></span> | <span data-ttu-id="31d61-118">Wert</span><span class="sxs-lookup"><span data-stu-id="31d61-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31d61-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31d61-119">Minimum supported client</span></span><br/> | <span data-ttu-id="31d61-120">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d61-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="31d61-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31d61-121">Minimum supported server</span></span><br/> | <span data-ttu-id="31d61-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d61-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="31d61-123">Header</span><span class="sxs-lookup"><span data-stu-id="31d61-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d61-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="31d61-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="31d61-125">Idl</span><span class="sxs-lookup"><span data-stu-id="31d61-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31d61-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="31d61-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="31d61-127">DLL</span><span class="sxs-lookup"><span data-stu-id="31d61-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31d61-128"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="31d61-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




