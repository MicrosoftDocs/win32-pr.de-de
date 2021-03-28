---
description: Gibt an, ob eine angegebene URL abonniert ist.
title: Shelluihelper. isabonniert-Methode (Exdisp. h)
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
ms.openlocfilehash: 2085f38e5f91f13a2f67ff4f22b003b533249386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042419"
---
# <a name="shelluihelperissubscribed-method"></a><span data-ttu-id="79502-103">Shelluihelper. isabonniert-Methode</span><span class="sxs-lookup"><span data-stu-id="79502-103">ShellUIHelper.IsSubscribed method</span></span>

<span data-ttu-id="79502-104">Gibt an, ob eine angegebene URL abonniert ist.</span><span class="sxs-lookup"><span data-stu-id="79502-104">Indicates whether a specified URL is subscribed to.</span></span>

## <a name="syntax"></a><span data-ttu-id="79502-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79502-105">Syntax</span></span>


```JScript
bRetVal = ShellUIHelper.IsSubscribed(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="79502-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79502-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79502-107">*sUrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79502-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79502-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="79502-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="79502-109">Ein **Zeichen** folgen Wert, der die URL angibt.</span><span class="sxs-lookup"><span data-stu-id="79502-109">A **String** value that specifies the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79502-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79502-110">Return value</span></span>

<span data-ttu-id="79502-111">Typ: \**Boolean \** _</span><span class="sxs-lookup"><span data-stu-id="79502-111">Type: \**Boolean\** _</span></span>

<span data-ttu-id="79502-112">_ \*true\*\*, wenn die URL abonniert ist; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="79502-112">_ *true*\* if the URL is subscribed to; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="79502-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79502-113">Examples</span></span>

<span data-ttu-id="79502-114">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript Embedded in HTML und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="79502-114">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="79502-115">JScript</span><span class="sxs-lookup"><span data-stu-id="79502-115">JScript:</span></span>


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



<span data-ttu-id="79502-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="79502-116">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="79502-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="79502-117">Requirements</span></span>



| <span data-ttu-id="79502-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79502-118">Requirement</span></span> | <span data-ttu-id="79502-119">Wert</span><span class="sxs-lookup"><span data-stu-id="79502-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79502-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79502-120">Minimum supported client</span></span><br/> | <span data-ttu-id="79502-121">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79502-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="79502-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79502-122">Minimum supported server</span></span><br/> | <span data-ttu-id="79502-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79502-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="79502-124">Header</span><span class="sxs-lookup"><span data-stu-id="79502-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="79502-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="79502-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="79502-126">DLL</span><span class="sxs-lookup"><span data-stu-id="79502-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79502-127"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="79502-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
