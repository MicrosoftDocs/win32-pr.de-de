---
description: Fügt der Liste der Kanäle im Windows Internet Explorer Favoritenmenü und der Kanalleiste auf dem Desktop einen neuen Kanal hinzu.
title: ShellUIHelper.AddChannel-Methode (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: d08c1360cb2a96fbc7b87daecb650bbf46aa6ad9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841201"
---
# <a name="shelluihelperaddchannel-method"></a><span data-ttu-id="ac503-103">ShellUIHelper.AddChannel-Methode</span><span class="sxs-lookup"><span data-stu-id="ac503-103">ShellUIHelper.AddChannel method</span></span>

<span data-ttu-id="ac503-104">Fügt der Liste der Kanäle im Menü Windows Internet Explorer **Favoriten**  und der Kanalleiste auf dem Desktop einen neuen Kanal hinzu.</span><span class="sxs-lookup"><span data-stu-id="ac503-104">Adds a new channel to the list of channels in the Windows Internet Explorer **Favorites** menu and to the **Channel** bar on the desktop.</span></span>

> [!Note]  
> <span data-ttu-id="ac503-105">Diese Methode wird unter Windows Vista nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ac503-105">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="ac503-106">Unter diesem Betriebssystem wird E \_ NOTIMPL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ac503-106">Under that operating system, it returns E\_NOTIMPL.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ac503-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac503-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="ac503-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac503-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac503-109">*sURL* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ac503-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac503-110">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ac503-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ac503-111">Ein **Zeichenfolgenwert,** der die URL der CDF-Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="ac503-111">A **String** value that specifies the URL of the CDF file.</span></span>

> [!Note]  
> <span data-ttu-id="ac503-112">Die Links in der CDF-Datei müssen http-, HTTPS- oder FTP-Protokolle verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac503-112">The links in the CDF file must use HTTP, HTTPS, or FTP protocols.</span></span> <span data-ttu-id="ac503-113">Wenn die CDF-Datei ein anderes Protokoll enthält, schlägt das Hinzufügen des Kanals fehl, und es wird kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac503-113">If the CDF file contains any other protocol, the addition of the channel fails and no dialog box appears.</span></span>

 

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ac503-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac503-114">Examples</span></span>

<span data-ttu-id="ac503-115">Im folgenden Beispiel wird die ordnungsgemäße Verwendung dieser Methode für JScript veranschaulicht, das in HTML und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ac503-115">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="ac503-116">Jscript:</span><span class="sxs-lookup"><span data-stu-id="ac503-116">JScript:</span></span>


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
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



<span data-ttu-id="ac503-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ac503-117">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ac503-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac503-118">Requirements</span></span>



| <span data-ttu-id="ac503-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac503-119">Requirement</span></span> | <span data-ttu-id="ac503-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ac503-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac503-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac503-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ac503-122">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac503-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ac503-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac503-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ac503-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac503-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ac503-125">Header</span><span class="sxs-lookup"><span data-stu-id="ac503-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac503-126"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ac503-126"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="ac503-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ac503-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac503-128"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ac503-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
