---
title: WebViewFolderContents.FocusedItem-Eigenschaft (Shldisp.h)
description: 'WebViewFolderContents.FocusedItem-Eigenschaft: Ruft ein FolderItem-Objekt ab, das das Element darstellt, das den Eingabefokus besitzt.'
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- FocusedItem-Eigenschaft Legacy-Windows-Umgebungsfeatures
- FocusedItem-Eigenschaft Legacy-Windows-Umgebungsfeatures, WebViewFolderContents-Objekt
- WebViewFolderContents-Objekt Legacy-Windows-Umgebungsfeatures , FocusedItem-Eigenschaft
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724743b81f605dc9ba5794a4a796b8a0c4a2a03f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102728"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a><span data-ttu-id="7fe63-106">WebViewFolderContents.FocusedItem-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7fe63-106">WebViewFolderContents.FocusedItem property</span></span>

<span data-ttu-id="7fe63-107">Ruft ein [**FolderItem-Objekt**](../shell/folderitem.md) ab, das das Element darstellt, das den Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="7fe63-107">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="7fe63-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7fe63-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fe63-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fe63-109">Syntax</span></span>


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="7fe63-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7fe63-110">Property value</span></span>

<span data-ttu-id="7fe63-111">Eine Variable vom Typ [IDispatch,](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) die das fokussierte Elementobjekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="7fe63-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="examples"></a><span data-ttu-id="7fe63-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fe63-112">Examples</span></span>

<span data-ttu-id="7fe63-113">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft in JScript, eingebettet in HTML.</span><span class="sxs-lookup"><span data-stu-id="7fe63-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="7fe63-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fe63-114">Requirements</span></span>



| <span data-ttu-id="7fe63-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7fe63-115">Requirement</span></span> | <span data-ttu-id="7fe63-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7fe63-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe63-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7fe63-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe63-118">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fe63-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7fe63-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7fe63-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe63-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7fe63-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7fe63-121">Header</span><span class="sxs-lookup"><span data-stu-id="7fe63-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fe63-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="7fe63-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7fe63-123">Idl</span><span class="sxs-lookup"><span data-stu-id="7fe63-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7fe63-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="7fe63-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7fe63-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7fe63-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fe63-126"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7fe63-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

