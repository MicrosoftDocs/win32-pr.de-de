---
title: Webviewfoldercontents. viewoptions-Eigenschaft (Shldisp. h)
description: Ruft einen Satz von shellfolderviewoptions-Flags ab, die die aktuellen Optionen der Ansicht angeben.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Viewoptions-Eigenschaft Legacy-Windows-Umgebungs Features
- Viewoptions-Eigenschaft Legacy-Windows-Umgebungs Funktionen, webviewfoldercontents-Objekt
- Webviewfoldercontents-Objekt Legacy Windows-Umgebungs Features, viewoptions-Eigenschaft
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040194"
---
# <a name="webviewfoldercontentsviewoptions-property"></a><span data-ttu-id="b4b1b-106">Webviewfoldercontents. viewoptions (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b4b1b-106">WebViewFolderContents.ViewOptions property</span></span>

<span data-ttu-id="b4b1b-107">Ruft einen Satz von [**shellfolderviewoptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) -Flags ab, die die aktuellen Optionen der Ansicht angeben.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-107">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span>

<span data-ttu-id="b4b1b-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b1b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4b1b-109">Syntax</span></span>


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="b4b1b-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b4b1b-110">Property value</span></span>

<span data-ttu-id="b4b1b-111">Eine Variable vom Typ [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , die das Ansichts Options Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span>

## <a name="examples"></a><span data-ttu-id="b4b1b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4b1b-112">Examples</span></span>

<span data-ttu-id="b4b1b-113">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft in JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="b4b1b-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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



## <a name="requirements"></a><span data-ttu-id="b4b1b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4b1b-114">Requirements</span></span>



| <span data-ttu-id="b4b1b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4b1b-115">Requirement</span></span> | <span data-ttu-id="b4b1b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b4b1b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b1b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4b1b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b1b-118">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4b1b-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b4b1b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4b1b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b1b-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4b1b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4b1b-121">Header</span><span class="sxs-lookup"><span data-stu-id="b4b1b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4b1b-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b1b-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b4b1b-123">IDL</span><span class="sxs-lookup"><span data-stu-id="b4b1b-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4b1b-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4b1b-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b4b1b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b4b1b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4b1b-126"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b4b1b-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

