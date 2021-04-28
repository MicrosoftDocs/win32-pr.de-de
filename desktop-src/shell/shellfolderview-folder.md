---
description: 'ShellFolderView.Folder-Eigenschaft: Ruft ein Folder-Objekt ab, das die Sicht darstellt.'
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: ShellFolderView.Folder-Eigenschaft (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 370fddc1428c8f77edb77cdac2dc04123fc5211f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083418"
---
# <a name="shellfolderviewfolder-property"></a><span data-ttu-id="f1f49-103">ShellFolderView.Folder-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f1f49-103">ShellFolderView.Folder property</span></span>

<span data-ttu-id="f1f49-104">Ruft ein [**Folder-Objekt**](folder.md) ab, das die Sicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="f1f49-104">Gets a [**Folder**](folder.md) object that represents the view.</span></span>

<span data-ttu-id="f1f49-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f1f49-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f49-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1f49-106">Syntax</span></span>


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a><span data-ttu-id="f1f49-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f1f49-107">Property value</span></span>

<span data-ttu-id="f1f49-108">Objekt, das das [**Folder-Objekt**](folder.md) empfängt.</span><span class="sxs-lookup"><span data-stu-id="f1f49-108">Object that receives the [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1f49-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1f49-109">Remarks</span></span>

<span data-ttu-id="f1f49-110">**Der Ordner** kann nur auf dem lokalen System aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f1f49-110">**Folder** can only be called on the local system.</span></span> <span data-ttu-id="f1f49-111">Sie funktioniert nicht, wenn sie auf einer Webseite über HTTP oder UNC ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1f49-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="f1f49-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1f49-112">Examples</span></span>

<span data-ttu-id="f1f49-113">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft für JScript, das in HTML eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="f1f49-113">The following example shows the proper usage of this property for JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
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
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="f1f49-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1f49-114">Requirements</span></span>



| <span data-ttu-id="f1f49-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1f49-115">Requirement</span></span> | <span data-ttu-id="f1f49-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f1f49-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f49-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1f49-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f1f49-118">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1f49-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f1f49-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1f49-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f1f49-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1f49-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f1f49-121">Header</span><span class="sxs-lookup"><span data-stu-id="f1f49-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1f49-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="f1f49-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f1f49-123">Idl</span><span class="sxs-lookup"><span data-stu-id="f1f49-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1f49-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1f49-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f1f49-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f1f49-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1f49-126"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="f1f49-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




