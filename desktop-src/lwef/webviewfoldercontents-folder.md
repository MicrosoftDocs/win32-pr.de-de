---
title: WebViewFolderContents.Folder-Eigenschaft (Shldisp.h)
description: 'WebViewFolderContents.Folder-Eigenschaft: Ruft ein Folder-Objekt ab, das die Ansicht darstellt.'
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Ordnereigenschaft Legacy-Windows-Umgebungsfeatures
- Ordnereigenschaft Legacy-Windows-Umgebungsfeatures , WebViewFolderContents-Objekt
- WebViewFolderContents-Objekt Legacy-Windows-Umgebungsfeatures , Folder-Eigenschaft
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88fd7a54971fa088bdddbc78d3d8df4af610875
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102698"
---
# <a name="webviewfoldercontentsfolder-property"></a><span data-ttu-id="4ca34-106">WebViewFolderContents.Folder-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4ca34-106">WebViewFolderContents.Folder property</span></span>

<span data-ttu-id="4ca34-107">Ruft ein [**Folder-Objekt**](../shell/folder.md) ab, das die Sicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="4ca34-107">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span>

<span data-ttu-id="4ca34-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4ca34-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca34-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ca34-109">Syntax</span></span>


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a><span data-ttu-id="4ca34-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4ca34-110">Property value</span></span>

<span data-ttu-id="4ca34-111">Ein -Objekt, das das [**Folder-Objekt**](../shell/folder.md) empfängt.</span><span class="sxs-lookup"><span data-stu-id="4ca34-111">An object that receives the [**Folder**](../shell/folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="4ca34-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ca34-112">Examples</span></span>

<span data-ttu-id="4ca34-113">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft in JScript, eingebettet in HTML.</span><span class="sxs-lookup"><span data-stu-id="4ca34-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
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



## <a name="requirements"></a><span data-ttu-id="4ca34-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ca34-114">Requirements</span></span>



| <span data-ttu-id="4ca34-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ca34-115">Requirement</span></span> | <span data-ttu-id="4ca34-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4ca34-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca34-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ca34-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca34-118">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ca34-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4ca34-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ca34-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca34-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ca34-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4ca34-121">Header</span><span class="sxs-lookup"><span data-stu-id="4ca34-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ca34-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="4ca34-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4ca34-123">Idl</span><span class="sxs-lookup"><span data-stu-id="4ca34-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4ca34-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="4ca34-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4ca34-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4ca34-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ca34-126"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="4ca34-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

