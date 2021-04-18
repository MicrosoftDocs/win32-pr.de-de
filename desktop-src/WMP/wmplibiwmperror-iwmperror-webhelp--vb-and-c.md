---
title: Iwmperror WebHelp-Methode
description: Die WebHelp-Methode öffnet die Windows Media Player-Webhilfe Seite, um weitere Informationen zum ersten Fehler in der Fehler Warteschlange anzuzeigen (Index null). | Iwmperror WebHelp-Methode
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- WebHelp-Methode (Windows Media Player)
- WebHelp-Methode, Windows Media Player, iwmperror-Schnittstelle
- Iwmperror Interface, Windows Media Player, WebHelp-Methode
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354772"
---
# <a name="iwmperrorwebhelp-method"></a><span data-ttu-id="3bba6-107">Iwmperror:: WebHelp-Methode</span><span class="sxs-lookup"><span data-stu-id="3bba6-107">IWMPError::webHelp method</span></span>

<span data-ttu-id="3bba6-108">Die **WebHelp** -Methode öffnet die Windows Media Player-Webhilfe Seite, um weitere Informationen zum ersten Fehler in der Fehler Warteschlange anzuzeigen (Index null).</span><span class="sxs-lookup"><span data-stu-id="3bba6-108">The **webHelp** method launches the Windows Media Player Web Help page to display further information about the first error in the error queue (index zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bba6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bba6-109">Syntax</span></span>


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a><span data-ttu-id="3bba6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bba6-110">Parameters</span></span>

<span data-ttu-id="3bba6-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3bba6-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3bba6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bba6-112">Return value</span></span>

<span data-ttu-id="3bba6-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3bba6-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bba6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bba6-114">Remarks</span></span>

<span data-ttu-id="3bba6-115">Die Web-Hilfeseiten enthalten stets die neuesten und detailliertesten Informationen zu Windows Media Player-Fehlern.</span><span class="sxs-lookup"><span data-stu-id="3bba6-115">The Web Help pages always contain the latest and most detailed information about Windows Media Player errors.</span></span> <span data-ttu-id="3bba6-116">Diese Methode überträgt automatisch die anderen Informationen, die von der Webhilfe benötigt werden, z. b. die verwendete Betriebssystemversion.</span><span class="sxs-lookup"><span data-stu-id="3bba6-116">This method automatically transfers the other information needed by Web Help, such as the operating system version being used.</span></span>

<span data-ttu-id="3bba6-117">Wenn Sie direkt auf die Web-Hilfeseiten zugreifen möchten, verwenden Sie die folgenden Links zu Fehlercode und Support Center:</span><span class="sxs-lookup"><span data-stu-id="3bba6-117">To access the Web Help pages directly, use the following error code and support center links:</span></span>

-   [<span data-ttu-id="3bba6-118">Windows Media Player-Fehler Code Informationen</span><span class="sxs-lookup"><span data-stu-id="3bba6-118">Windows Media Player Error Code Information</span></span>](https://support.microsoft.com/kb/886273)
-   [<span data-ttu-id="3bba6-119">Windows Media Player-Lösungs Center</span><span class="sxs-lookup"><span data-stu-id="3bba6-119">Windows Media Player Solution Center</span></span>](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a><span data-ttu-id="3bba6-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3bba6-120">Examples</span></span>

<span data-ttu-id="3bba6-121">Im folgenden Beispiel wird eine Schaltfläche erstellt, mit der die Microsoft Windows Media Player-Webhilfe Seite im Browser gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="3bba6-121">The following example creates a button that launches the Microsoft Windows Media Player Web Help page in the browser.</span></span> <span data-ttu-id="3bba6-122">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3bba6-122">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3bba6-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bba6-123">Requirements</span></span>



| <span data-ttu-id="3bba6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bba6-124">Requirement</span></span> | <span data-ttu-id="3bba6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3bba6-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bba6-126">Version</span><span class="sxs-lookup"><span data-stu-id="3bba6-126">Version</span></span><br/>   | <span data-ttu-id="3bba6-127">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="3bba6-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3bba6-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="3bba6-128">Namespace</span></span><br/> | <span data-ttu-id="3bba6-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3bba6-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3bba6-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="3bba6-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3bba6-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3bba6-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bba6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bba6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bba6-133">**Iwmperror-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3bba6-133">**IWMPError Interface (VB and C#)**</span></span>](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





