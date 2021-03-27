---
description: Zeigt die Standardbenutzer Oberfläche zum Erstellen eines bevorzugten Elements an. Die Benutzeroberfläche wird mit den angegebenen Parametern initialisiert.
title: Shelluihelper. addfavorit-Methode (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: a5c3cae52f0ad18c1f2ddf6cf91759d1c6daf6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980721"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="12407-104">Shelluihelper. addfavorit-Methode</span><span class="sxs-lookup"><span data-stu-id="12407-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="12407-105">Zeigt die Standardbenutzer Oberfläche zum Erstellen eines bevorzugten Elements an.</span><span class="sxs-lookup"><span data-stu-id="12407-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="12407-106">Die Benutzeroberfläche wird mit den angegebenen Parametern initialisiert.</span><span class="sxs-lookup"><span data-stu-id="12407-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="12407-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="12407-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="12407-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="12407-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12407-109">*sUrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12407-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12407-110">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="12407-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="12407-111">Ein **Zeichen** folgen Wert, der die URL des Elements angibt, das dem Ordner **Favoriten** hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="12407-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="12407-112">*vtitle* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="12407-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="12407-113">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="12407-113">Type: \**Variant\** _</span></span>

<span data-ttu-id="12407-114">Ein _ \*Variant\*\*-Wert, der den Namen des Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="12407-114">A _ *Variant*\* value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="12407-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12407-115">Examples</span></span>

<span data-ttu-id="12407-116">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript Embedded in HTML und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="12407-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="12407-117">JScript</span><span class="sxs-lookup"><span data-stu-id="12407-117">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



<span data-ttu-id="12407-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="12407-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="12407-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="12407-119">Requirements</span></span>



| <span data-ttu-id="12407-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12407-120">Requirement</span></span> | <span data-ttu-id="12407-121">Wert</span><span class="sxs-lookup"><span data-stu-id="12407-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12407-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12407-122">Minimum supported client</span></span><br/> | <span data-ttu-id="12407-123">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12407-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="12407-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12407-124">Minimum supported server</span></span><br/> | <span data-ttu-id="12407-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12407-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12407-126">Header</span><span class="sxs-lookup"><span data-stu-id="12407-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="12407-127"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="12407-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="12407-128">DLL</span><span class="sxs-lookup"><span data-stu-id="12407-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12407-129"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="12407-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
