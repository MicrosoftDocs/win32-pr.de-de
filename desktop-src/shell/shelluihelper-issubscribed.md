---
description: Gibt an, ob eine angegebene URL abonniert wird.
title: ShellUIHelper.IsSubkribierte Methode (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.IsSubscribed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: fcf23352-6603-4b17-9c3b-b353cca1c003
ms.openlocfilehash: ca68d2e46ce74593b66aac6f995b88ddcb79796b
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842491"
---
# <a name="shelluihelperissubscribed-method"></a><span data-ttu-id="a8baf-103">ShellUIHelper.IsSubkribierte Methode</span><span class="sxs-lookup"><span data-stu-id="a8baf-103">ShellUIHelper.IsSubscribed method</span></span>

<span data-ttu-id="a8baf-104">Gibt an, ob eine angegebene URL abonniert wird.</span><span class="sxs-lookup"><span data-stu-id="a8baf-104">Indicates whether a specified URL is subscribed to.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8baf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8baf-105">Syntax</span></span>


```JScript
bRetVal = ShellUIHelper.IsSubscribed(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="a8baf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8baf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8baf-107">*sURL* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a8baf-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8baf-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a8baf-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a8baf-109">Ein  Zeichenfolgenwert, der die URL angibt.</span><span class="sxs-lookup"><span data-stu-id="a8baf-109">A **String** value that specifies the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8baf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8baf-110">Return value</span></span>

<span data-ttu-id="a8baf-111">Typ: **Boolean \***</span><span class="sxs-lookup"><span data-stu-id="a8baf-111">Type: **Boolean\***</span></span>

<span data-ttu-id="a8baf-112">**TRUE,** wenn die URL abonniert ist; andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a8baf-112">**true** if the URL is subscribed to; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="a8baf-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8baf-113">Examples</span></span>

<span data-ttu-id="a8baf-114">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript, das in HTML und Visual Basic eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="a8baf-114">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="a8baf-115">Jscript:</span><span class="sxs-lookup"><span data-stu-id="a8baf-115">JScript:</span></span>


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
    function fnShellUIHelperIsSubscribedJ()
    {
        var bReturn;
        
        bReturn = ShellUIHelper.IsSubscribed("https://www.microsoft.com/");
        alert(bReturn);
    }
</script>

</head>
<body onload=fnShellUIHelperIsSubscribedJ()>
</body>
</html>
```



<span data-ttu-id="a8baf-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a8baf-116">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperIsSubscribedVB()
    Dim objShellUIHelper As ShellUIHelper
    Dim bReturn          As Boolean
    
    Set objShellUIHelper = New ShellUIHelper
        bReturn = objShellUIHelper.IsSubscribed("https://www.microsoft.com/")
        Debug.Print bReturn
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a8baf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8baf-117">Requirements</span></span>



| <span data-ttu-id="a8baf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8baf-118">Requirement</span></span> | <span data-ttu-id="a8baf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a8baf-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8baf-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8baf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a8baf-121">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8baf-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a8baf-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8baf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a8baf-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8baf-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a8baf-124">Header</span><span class="sxs-lookup"><span data-stu-id="a8baf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8baf-125"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a8baf-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="a8baf-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a8baf-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8baf-127"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a8baf-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
