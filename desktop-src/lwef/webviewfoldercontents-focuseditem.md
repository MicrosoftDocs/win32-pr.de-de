---
title: Webviewfoldercontents. FocusedItem-Eigenschaft (Shldisp. h)
description: Ruft ein folderItem-Objekt ab, das das Element darstellt, das den Eingabefokus besitzt.
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- Eigenschaften der FocusedItem-Eigenschaft Legacy-Windows-Umgebung
- FocusedItem-Eigenschaft Legacy Windows-Umgebungs Funktionen, webviewfoldercontents-Objekt
- Webviewfoldercontents-Objekt Legacy Funktionen der Windows-Umgebung, FocusedItem (Eigenschaft)
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
ms.openlocfilehash: 050e7c2a4c280a949ec3684e2b05610830315a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391554"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a><span data-ttu-id="30b99-106">Webviewfoldercontents. FocusedItem (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="30b99-106">WebViewFolderContents.FocusedItem property</span></span>

<span data-ttu-id="30b99-107">Ruft ein [**folderItem**](../shell/folderitem.md) -Objekt ab, das das Element darstellt, das den Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="30b99-107">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="30b99-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="30b99-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b99-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="30b99-109">Syntax</span></span>


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="30b99-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="30b99-110">Property value</span></span>

<span data-ttu-id="30b99-111">Eine Variable vom Typ [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , die das Objekt mit dem Fokus Element empfängt.</span><span class="sxs-lookup"><span data-stu-id="30b99-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="examples"></a><span data-ttu-id="30b99-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30b99-112">Examples</span></span>

<span data-ttu-id="30b99-113">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft in JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="30b99-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="30b99-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30b99-114">Requirements</span></span>



| <span data-ttu-id="30b99-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30b99-115">Requirement</span></span> | <span data-ttu-id="30b99-116">Wert</span><span class="sxs-lookup"><span data-stu-id="30b99-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b99-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30b99-117">Minimum supported client</span></span><br/> | <span data-ttu-id="30b99-118">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30b99-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="30b99-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30b99-119">Minimum supported server</span></span><br/> | <span data-ttu-id="30b99-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30b99-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="30b99-121">Header</span><span class="sxs-lookup"><span data-stu-id="30b99-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="30b99-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="30b99-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="30b99-123">IDL</span><span class="sxs-lookup"><span data-stu-id="30b99-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30b99-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30b99-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="30b99-125">DLL</span><span class="sxs-lookup"><span data-stu-id="30b99-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30b99-126"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="30b99-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

