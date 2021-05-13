---
description: Zeigt die Standardbenutzerschnittstelle zum Erstellen eines bevorzugten Elements an. Die Benutzeroberfläche wird mit den angegebenen Parametern initialisiert.
title: ShellUIHelper.AddFavorite-Methode (Exdisp.h)
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
ms.openlocfilehash: 2ce6fa0a71bb2ab995e510f06b4403c78bebcc60
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842451"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="79330-104">ShellUIHelper.AddFavorite-Methode</span><span class="sxs-lookup"><span data-stu-id="79330-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="79330-105">Zeigt die Standardbenutzerschnittstelle zum Erstellen eines bevorzugten Elements an.</span><span class="sxs-lookup"><span data-stu-id="79330-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="79330-106">Die Benutzeroberfläche wird mit den angegebenen Parametern initialisiert.</span><span class="sxs-lookup"><span data-stu-id="79330-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="79330-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="79330-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="79330-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="79330-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79330-109">*sURL* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="79330-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79330-110">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="79330-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="79330-111">Ein  Zeichenfolgenwert, der die URL des Elements angibt, das dem Ordner **Favoriten** hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="79330-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="79330-112">*vTitle* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="79330-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79330-113">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="79330-113">Type: **Variant\***</span></span>

<span data-ttu-id="79330-114">Ein **Variant-Wert,** der den Namen des Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="79330-114">A **Variant** value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="79330-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79330-115">Examples</span></span>

<span data-ttu-id="79330-116">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript, das in HTML und Visual Basic eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="79330-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="79330-117">Jscript:</span><span class="sxs-lookup"><span data-stu-id="79330-117">JScript:</span></span>


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



<span data-ttu-id="79330-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="79330-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="79330-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79330-119">Requirements</span></span>



| <span data-ttu-id="79330-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79330-120">Requirement</span></span> | <span data-ttu-id="79330-121">Wert</span><span class="sxs-lookup"><span data-stu-id="79330-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79330-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79330-122">Minimum supported client</span></span><br/> | <span data-ttu-id="79330-123">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79330-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="79330-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79330-124">Minimum supported server</span></span><br/> | <span data-ttu-id="79330-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79330-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="79330-126">Header</span><span class="sxs-lookup"><span data-stu-id="79330-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="79330-127"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="79330-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="79330-128">DLL</span><span class="sxs-lookup"><span data-stu-id="79330-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79330-129"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="79330-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
