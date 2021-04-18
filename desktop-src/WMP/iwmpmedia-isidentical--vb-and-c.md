---
title: Iwmpmedia. isidentical (VB und C)
description: Mit der isidentical-Eigenschaft (der get \_ isidentical-Methode in C \) wird ein Wert abgerufen, der angibt, ob das angegebene Medien Element mit dem aktuellen übereinstimmt.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- Iwmpmedia. isidentical (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372201"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a><span data-ttu-id="39fe6-104">Iwmpmedia. isidentical (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="39fe6-104">IWMPMedia.isIdentical (VB and C#)</span></span>

<span data-ttu-id="39fe6-105">Mit der **isidentical** -Eigenschaft (der **get \_ isidentical** -Methode in c#) wird ein Wert abgerufen, der angibt, ob das angegebene Medien Element mit dem aktuellen übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="39fe6-105">The **isIdentical** property (the **get\_isIdentical** method in C#) gets a value indicating whether the specified media item is the same as the current one.</span></span>


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a><span data-ttu-id="39fe6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="39fe6-106">Parameters</span></span>

<span data-ttu-id="39fe6-107">*piwmpmedia*</span><span class="sxs-lookup"><span data-stu-id="39fe6-107">*pIWMPMedia*</span></span>

<span data-ttu-id="39fe6-108">Eine **WMPLib. iwmpmedia** -Schnittstelle für das Medien Element, das mit dem aktuellen Medien Element verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="39fe6-108">A **WMPLib.IWMPMedia** interface to the media item to be compared with the current media item.</span></span>

## <a name="property-value"></a><span data-ttu-id="39fe6-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="39fe6-109">Property Value</span></span>

<span data-ttu-id="39fe6-110">Ein **System. Boolean** -Wert, der angibt, ob die beiden Medienelemente identisch sind.</span><span class="sxs-lookup"><span data-stu-id="39fe6-110">A **System.Boolean** value that indicates whether the two media items are identical.</span></span>

## <a name="remarks"></a><span data-ttu-id="39fe6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39fe6-111">Remarks</span></span>

<span data-ttu-id="39fe6-112">**Iwmpmedia. isidentical** ist eine Eigenschaft in Visual Basic, die einen-Parameter annimmt.</span><span class="sxs-lookup"><span data-stu-id="39fe6-112">**IWMPMedia.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="39fe6-113">In c# wird dies als **iwmpmedia. get \_ isidentical** -Methode bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="39fe6-113">In C# it is referred to as the **IWMPMedia.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="39fe6-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39fe6-114">Examples</span></span>

<span data-ttu-id="39fe6-115">Im folgenden Beispiel wird die **isidentical** -Eigenschaft (die **get \_ isidentical** -Methode in c#) verwendet, um zu überprüfen, ob ein Medien Element mit dem Namen newmedia mit dem aktuellen Medien Element identisch ist.</span><span class="sxs-lookup"><span data-stu-id="39fe6-115">The following example uses the **isIdentical** property (the **get\_isIdentical** method in C#) to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="39fe6-116">Wenn Sie nicht identisch sind, wird das neue Medien Element wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="39fe6-116">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="39fe6-117">Andernfalls wird das aktuelle Medium weiterhin ununterbrochen abgespielt.</span><span class="sxs-lookup"><span data-stu-id="39fe6-117">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="39fe6-118">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="39fe6-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

End If
```





## <a name="requirements"></a><span data-ttu-id="39fe6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39fe6-119">Requirements</span></span>



| <span data-ttu-id="39fe6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39fe6-120">Requirement</span></span> | <span data-ttu-id="39fe6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="39fe6-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39fe6-122">Version</span><span class="sxs-lookup"><span data-stu-id="39fe6-122">Version</span></span><br/>   | <span data-ttu-id="39fe6-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="39fe6-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="39fe6-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="39fe6-124">Namespace</span></span><br/> | <span data-ttu-id="39fe6-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="39fe6-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="39fe6-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="39fe6-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="39fe6-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="39fe6-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39fe6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39fe6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39fe6-129">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="39fe6-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





