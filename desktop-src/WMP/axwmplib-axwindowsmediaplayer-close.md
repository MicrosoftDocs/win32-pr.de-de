---
title: AxWindowsMediaPlayer. Close-Methode
description: Die Close-Methode schließt die aktuelle digitale Mediendatei, beendet die Wiedergabe in Windows Media Player und gibt Windows Media Player-Ressourcen frei.
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- Schließen von Methoden Fenstern Media Player
- Close-Methode, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, Close-Methode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366980"
---
# <a name="axwindowsmediaplayerclose-method"></a><span data-ttu-id="7a6a7-106">AxWindowsMediaPlayer. Close-Methode</span><span class="sxs-lookup"><span data-stu-id="7a6a7-106">AxWindowsMediaPlayer.close method</span></span>

<span data-ttu-id="7a6a7-107">Die Close-Methode schließt die aktuelle digitale Mediendatei, beendet die Wiedergabe in Windows Media Player und gibt Windows Media Player-Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-107">The close method closes the current digital media file, stops playback in Windows Media Player and releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a6a7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a6a7-108">Syntax</span></span>


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a><span data-ttu-id="7a6a7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a6a7-109">Parameters</span></span>

<span data-ttu-id="7a6a7-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a6a7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a6a7-111">Return value</span></span>

<span data-ttu-id="7a6a7-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a6a7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a6a7-113">Remarks</span></span>

<span data-ttu-id="7a6a7-114">Diese Methode schließt die aktuelle digitale Mediendatei, nicht Windows Media Player selbst.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="7a6a7-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a6a7-115">Examples</span></span>

<span data-ttu-id="7a6a7-116">Im folgenden Beispiel wird eine Schaltfläche erstellt, bei der die Wiedergabe in Windows Media Player beendet wird und die verwendeten Ressourcen freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-116">The following example creates a button that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="7a6a7-117">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7a6a7-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="7a6a7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a6a7-118">Requirements</span></span>



| <span data-ttu-id="7a6a7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a6a7-119">Requirement</span></span> | <span data-ttu-id="7a6a7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7a6a7-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a6a7-121">Version</span><span class="sxs-lookup"><span data-stu-id="7a6a7-121">Version</span></span><br/>   | <span data-ttu-id="7a6a7-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="7a6a7-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7a6a7-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a6a7-123">Namespace</span></span><br/> | <span data-ttu-id="7a6a7-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7a6a7-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7a6a7-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="7a6a7-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7a6a7-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7a6a7-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a6a7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a6a7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a6a7-128">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="7a6a7-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





