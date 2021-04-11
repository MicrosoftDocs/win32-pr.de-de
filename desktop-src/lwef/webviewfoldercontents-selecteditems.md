---
title: WebViewFolderContents.SelectedItems-Methode (Shldisp.h)
description: Ruft ein folderitems-Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- SelectedItems-Methode Legacy-Windows-Umgebungs Features
- SelectedItems-Methode Legacy-Windows-Umgebungs Features, webviewfoldercontents-Objekt
- Webviewfoldercontents-Objekt Legacy Funktionen der Windows-Umgebung, SelectedItems-Methode
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
ms.openlocfilehash: cee4b7f34cdcabec637671af79775fc1fa546790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040917"
---
# <a name="webviewfoldercontentsselecteditems-method"></a><span data-ttu-id="2ddfe-106">Webviewfoldercontents. SelectedItems-Methode</span><span class="sxs-lookup"><span data-stu-id="2ddfe-106">WebViewFolderContents.SelectedItems method</span></span>

<span data-ttu-id="2ddfe-107">Ruft ein [**folderitems**](../shell/folderitems.md) -Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="2ddfe-107">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ddfe-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ddfe-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="2ddfe-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ddfe-109">Parameters</span></span>

<span data-ttu-id="2ddfe-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2ddfe-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ddfe-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ddfe-111">Return value</span></span>

<span data-ttu-id="2ddfe-112">Type: **[ **folderitems**](../shell/folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2ddfe-112">Type: **[**FolderItems**](../shell/folderitems.md)\*\***</span></span>

<span data-ttu-id="2ddfe-113">Ein Objekt Verweis auf das [**folderitems**](../shell/folderitems.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2ddfe-113">An object reference to the [**FolderItems**](../shell/folderitems.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="2ddfe-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ddfe-114">Examples</span></span>

<span data-ttu-id="2ddfe-115">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="2ddfe-115">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2ddfe-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ddfe-116">Requirements</span></span>



| <span data-ttu-id="2ddfe-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ddfe-117">Requirement</span></span> | <span data-ttu-id="2ddfe-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2ddfe-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddfe-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ddfe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2ddfe-120">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ddfe-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2ddfe-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ddfe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2ddfe-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ddfe-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2ddfe-123">Header</span><span class="sxs-lookup"><span data-stu-id="2ddfe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ddfe-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ddfe-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2ddfe-125">IDL</span><span class="sxs-lookup"><span data-stu-id="2ddfe-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2ddfe-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2ddfe-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2ddfe-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2ddfe-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ddfe-128"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="2ddfe-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

