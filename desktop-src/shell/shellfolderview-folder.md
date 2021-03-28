---
description: Ruft ein Ordner Objekt ab, das die Ansicht darstellt.
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: Shellfolderview. Folder-Eigenschaft (Shldisp. h)
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
ms.openlocfilehash: 40590064048ba5410dc9341791aec443f16d68e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217695"
---
# <a name="shellfolderviewfolder-property"></a><span data-ttu-id="4e8a1-103">Shellfolderview. Folder (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4e8a1-103">ShellFolderView.Folder property</span></span>

<span data-ttu-id="4e8a1-104">Ruft ein [**Ordner**](folder.md) Objekt ab, das die Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="4e8a1-104">Gets a [**Folder**](folder.md) object that represents the view.</span></span>

<span data-ttu-id="4e8a1-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4e8a1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e8a1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e8a1-106">Syntax</span></span>


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a><span data-ttu-id="4e8a1-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4e8a1-107">Property value</span></span>

<span data-ttu-id="4e8a1-108">Objekt, das das [**Ordner**](folder.md) Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="4e8a1-108">Object that receives the [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e8a1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e8a1-109">Remarks</span></span>

<span data-ttu-id="4e8a1-110">Der **Ordner** kann nur auf dem lokalen System aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4e8a1-110">**Folder** can only be called on the local system.</span></span> <span data-ttu-id="4e8a1-111">Es funktioniert nicht, wenn es auf einer Webseite über HTTP oder UNC ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e8a1-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="4e8a1-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e8a1-112">Examples</span></span>

<span data-ttu-id="4e8a1-113">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft für JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="4e8a1-113">The following example shows the proper usage of this property for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4e8a1-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="4e8a1-114">Requirements</span></span>



| <span data-ttu-id="4e8a1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e8a1-115">Requirement</span></span> | <span data-ttu-id="4e8a1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4e8a1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e8a1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e8a1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4e8a1-118">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e8a1-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4e8a1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e8a1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4e8a1-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e8a1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4e8a1-121">Header</span><span class="sxs-lookup"><span data-stu-id="4e8a1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e8a1-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e8a1-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4e8a1-123">IDL</span><span class="sxs-lookup"><span data-stu-id="4e8a1-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4e8a1-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4e8a1-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4e8a1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4e8a1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e8a1-126"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="4e8a1-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




