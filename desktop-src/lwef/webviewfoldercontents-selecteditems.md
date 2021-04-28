---
title: WebViewFolderContents.SelectedItems-Methode (Shldisp.h)
description: 'WebViewFolderContents.SelectedItems-Methode: Ruft ein FolderItems-Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.'
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- SelectedItems-Methode Legacy-Windows-Umgebungsfeatures
- SelectedItems-Methode Legacy-Windows-Umgebungsfeatures, WebViewFolderContents-Objekt
- WebViewFolderContents-Objekt Legacy-Windows-Umgebungsfeatures, SelectedItems-Methode
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a242991f6f9472610dffa20593f9cab5d8c310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102648"
---
# <a name="webviewfoldercontentsselecteditems-method"></a><span data-ttu-id="b265c-106">WebViewFolderContents.SelectedItems-Methode</span><span class="sxs-lookup"><span data-stu-id="b265c-106">WebViewFolderContents.SelectedItems method</span></span>

<span data-ttu-id="b265c-107">Ruft ein [**FolderItems-Objekt**](../shell/folderitems.md) ab, das alle ausgewählten Elemente in der Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="b265c-107">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="b265c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b265c-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="b265c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b265c-109">Parameters</span></span>

<span data-ttu-id="b265c-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b265c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b265c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b265c-111">Return value</span></span>

<span data-ttu-id="b265c-112">Typ: **[ **FolderItems**](../shell/folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b265c-112">Type: **[**FolderItems**](../shell/folderitems.md)\*\***</span></span>

<span data-ttu-id="b265c-113">Ein Objektverweis auf das [**FolderItems-Objekt.**](../shell/folderitems.md)</span><span class="sxs-lookup"><span data-stu-id="b265c-113">An object reference to the [**FolderItems**](../shell/folderitems.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="b265c-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b265c-114">Examples</span></span>

<span data-ttu-id="b265c-115">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für in HTML eingebettetes JScript.</span><span class="sxs-lookup"><span data-stu-id="b265c-115">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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



## <a name="requirements"></a><span data-ttu-id="b265c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b265c-116">Requirements</span></span>



| <span data-ttu-id="b265c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b265c-117">Requirement</span></span> | <span data-ttu-id="b265c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b265c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b265c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b265c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b265c-120">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b265c-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b265c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b265c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b265c-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b265c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b265c-123">Header</span><span class="sxs-lookup"><span data-stu-id="b265c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b265c-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b265c-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b265c-125">Idl</span><span class="sxs-lookup"><span data-stu-id="b265c-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b265c-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="b265c-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b265c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b265c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b265c-128"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b265c-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

