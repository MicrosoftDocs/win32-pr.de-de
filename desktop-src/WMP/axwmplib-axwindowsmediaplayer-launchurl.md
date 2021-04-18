---
title: AxWindowsMediaPlayer. launchurl-Methode
description: Die launchurl-Methode sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll. | AxWindowsMediaPlayer. launchurl-Methode
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- launchurl-Methode, Windows Media Player
- launchurl-Methode, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, launchurl-Methode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27fe8e544bb14b119785b26b9cb5be5cdad48015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372233"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a><span data-ttu-id="f66db-107">AxWindowsMediaPlayer. launchurl-Methode</span><span class="sxs-lookup"><span data-stu-id="f66db-107">AxWindowsMediaPlayer.launchURL method</span></span>

<span data-ttu-id="f66db-108">Die launchurl-Methode sendet eine URL an den Standardbrowser des Benutzers, der gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f66db-108">The launchURL method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="f66db-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f66db-109">Syntax</span></span>


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="f66db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f66db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f66db-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="f66db-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="f66db-112">Die **System. String** -URL, die die zu startende URL ist.</span><span class="sxs-lookup"><span data-stu-id="f66db-112">The **System.String** that is the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f66db-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f66db-113">Return value</span></span>

<span data-ttu-id="f66db-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f66db-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f66db-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f66db-115">Remarks</span></span>

<span data-ttu-id="f66db-116">Diese Methode öffnet nur Webseiten mithilfe der http-oder HTTPS-Protokolle.</span><span class="sxs-lookup"><span data-stu-id="f66db-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

## <a name="examples"></a><span data-ttu-id="f66db-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f66db-117">Examples</span></span>

<span data-ttu-id="f66db-118">Im folgenden Beispiel wird eine Schaltfläche erstellt, bei der die Microsoft-Website in einem neuen Browserfenster angezeigt wird, wenn darauf geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="f66db-118">The following example creates a button that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="f66db-119">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f66db-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f66db-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f66db-120">Requirements</span></span>



| <span data-ttu-id="f66db-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f66db-121">Requirement</span></span> | <span data-ttu-id="f66db-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f66db-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f66db-123">Version</span><span class="sxs-lookup"><span data-stu-id="f66db-123">Version</span></span><br/>   | <span data-ttu-id="f66db-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="f66db-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f66db-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f66db-125">Namespace</span></span><br/> | <span data-ttu-id="f66db-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f66db-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f66db-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="f66db-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f66db-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f66db-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f66db-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f66db-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f66db-130">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f66db-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





