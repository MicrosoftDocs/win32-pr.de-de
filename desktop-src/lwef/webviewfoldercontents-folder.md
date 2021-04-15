---
title: WebViewFolderContents.Folder-Eigenschaft (Shldisp.h)
description: Ruft ein Ordner Objekt ab, das die Ansicht darstellt.
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Ordner Eigenschaft Legacy-Windows-Umgebungs Features
- Ordner Eigenschaft Legacy Windows-Umgebungs Funktionen, webviewfoldercontents-Objekt
- Webviewfoldercontents-Objekt Legacy-Windows-Umgebungs Features, Ordner Eigenschaft
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
ms.openlocfilehash: 4c0640d4e29b903b32a6c9ed1e0b1de9f458b132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475423"
---
# <a name="webviewfoldercontentsfolder-property"></a><span data-ttu-id="b42bf-106">Webviewfoldercontents. Folder-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b42bf-106">WebViewFolderContents.Folder property</span></span>

<span data-ttu-id="b42bf-107">Ruft ein [**Ordner**](../shell/folder.md) Objekt ab, das die Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="b42bf-107">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span>

<span data-ttu-id="b42bf-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b42bf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b42bf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b42bf-109">Syntax</span></span>


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a><span data-ttu-id="b42bf-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b42bf-110">Property value</span></span>

<span data-ttu-id="b42bf-111">Ein Objekt, das das [**Ordner**](../shell/folder.md) Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="b42bf-111">An object that receives the [**Folder**](../shell/folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="b42bf-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b42bf-112">Examples</span></span>

<span data-ttu-id="b42bf-113">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft in JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="b42bf-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b42bf-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b42bf-114">Requirements</span></span>



| <span data-ttu-id="b42bf-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b42bf-115">Requirement</span></span> | <span data-ttu-id="b42bf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b42bf-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b42bf-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b42bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b42bf-118">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b42bf-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b42bf-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b42bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b42bf-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b42bf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b42bf-121">Header</span><span class="sxs-lookup"><span data-stu-id="b42bf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b42bf-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b42bf-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b42bf-123">IDL</span><span class="sxs-lookup"><span data-stu-id="b42bf-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b42bf-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b42bf-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b42bf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b42bf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b42bf-126"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b42bf-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

