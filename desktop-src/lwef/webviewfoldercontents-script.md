---
title: Webviewfoldercontents. Script-Eigenschaft (Shldisp. h)
description: Ruft das Skript Objekt für die Ansicht ab.
ms.assetid: f65246c5-3cd6-43bd-b267-ad27bdd0b41e
keywords:
- Skript Eigenschaften Legacy-Windows-Umgebungs Features
- Skript Eigenschaft Legacy-Windows-Umgebungs Funktionen, webviewfoldercontents-Objekt
- Webviewfoldercontents-Objekt Legacy-Windows-Umgebungs Funktionen, Skript Eigenschaft
topic_type:
- apiref
api_name:
- WebViewFolderContents.Script
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92133278d73851fa43353c116a2385da9b0fd3da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343875"
---
# <a name="webviewfoldercontentsscript-property"></a><span data-ttu-id="de74a-106">Webviewfoldercontents. Script (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="de74a-106">WebViewFolderContents.Script property</span></span>

<span data-ttu-id="de74a-107">Ruft das Skript Objekt für die Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="de74a-107">Gets the scripting object for the view.</span></span>

<span data-ttu-id="de74a-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="de74a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="de74a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="de74a-109">Syntax</span></span>


```JScript
objScript = WebViewFolderContents.Script
```



## <a name="property-value"></a><span data-ttu-id="de74a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="de74a-110">Property value</span></span>

<span data-ttu-id="de74a-111">Eine Variable vom Typ [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , die das Skript Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="de74a-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the scripting object.</span></span>

## <a name="examples"></a><span data-ttu-id="de74a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de74a-112">Examples</span></span>

<span data-ttu-id="de74a-113">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Eigenschaft in JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="de74a-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsScriptJ()
    {
        var objScript;

        objScript = FileList.Script;
        if (objScript != null)
        {
            alert(objScript.Name);
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



## <a name="requirements"></a><span data-ttu-id="de74a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de74a-114">Requirements</span></span>



| <span data-ttu-id="de74a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de74a-115">Requirement</span></span> | <span data-ttu-id="de74a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="de74a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de74a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de74a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de74a-118">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de74a-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="de74a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de74a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de74a-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de74a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="de74a-121">Header</span><span class="sxs-lookup"><span data-stu-id="de74a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="de74a-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de74a-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="de74a-123">IDL</span><span class="sxs-lookup"><span data-stu-id="de74a-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="de74a-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="de74a-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="de74a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="de74a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de74a-126"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="de74a-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

