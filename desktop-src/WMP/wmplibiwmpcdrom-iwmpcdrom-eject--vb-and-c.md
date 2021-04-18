---
title: Iwmpcdrom Auswerfen-Methode
description: Die Auswerfen-Methode fügt die CD oder DVD vom Laufwerk ein. | Iwmpcdrom Auswerfen-Methode
ms.assetid: c0a69252-fd79-452c-bc61-3c3e8bcaaf48
keywords:
- Auswerfen-Methode, Windows-Media Player
- Auswerfen-Methode, Windows Media Player, iwmpcdrom-Schnittstelle
- Iwmpcdrom-Schnittstelle, Windows Media Player, Auswerfen-Methode
topic_type:
- apiref
api_name:
- IWMPCdrom.eject
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ca2403b86b648e98861d91a21db80ddb64aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371621"
---
# <a name="iwmpcdromeject-method"></a><span data-ttu-id="2137a-107">Iwmpcdrom:: eject-Methode</span><span class="sxs-lookup"><span data-stu-id="2137a-107">IWMPCdrom::eject method</span></span>

<span data-ttu-id="2137a-108">Die **auswerfen** -Methode fügt die CD oder DVD vom Laufwerk ein.</span><span class="sxs-lookup"><span data-stu-id="2137a-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="2137a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2137a-109">Syntax</span></span>


```CSharp
public void eject();
```


```VB

Public Sub eject()
Implements IWMPCdrom.eject
```





## <a name="parameters"></a><span data-ttu-id="2137a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2137a-110">Parameters</span></span>

<span data-ttu-id="2137a-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2137a-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2137a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2137a-112">Return value</span></span>

<span data-ttu-id="2137a-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2137a-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2137a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2137a-114">Remarks</span></span>

<span data-ttu-id="2137a-115">Wenn die Laufwerks Tür geöffnet ist, schließt diese Methode die Tür.</span><span class="sxs-lookup"><span data-stu-id="2137a-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="2137a-116">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2137a-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="2137a-117">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2137a-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2137a-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2137a-118">Examples</span></span>

<span data-ttu-id="2137a-119">Im folgenden Beispiel wird **auswerfen** verwendet, um die Tür des CD-oder DVD-Laufwerks mit dem Index 0 (null) als Reaktion auf das Click-Ereignis einer Schaltfläche zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2137a-119">The following example uses **eject** to open the door of the CD or DVD drive that has the index of zero in response to the Click event of a button.</span></span> <span data-ttu-id="2137a-120">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2137a-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void ejectButton_Click(object o, System.EventArgs args)
{
    player.cdromCollection.Item(0).eject();
}
```


```VB

Public Sub ejectButton_Click(ByVal o As Object, ByVal args As System.EventArgs) Handles ejectButton.Click

    player.cdromCollection.Item(0).eject()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2137a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2137a-121">Requirements</span></span>



| <span data-ttu-id="2137a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2137a-122">Requirement</span></span> | <span data-ttu-id="2137a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2137a-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2137a-124">Version</span><span class="sxs-lookup"><span data-stu-id="2137a-124">Version</span></span><br/>   | <span data-ttu-id="2137a-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="2137a-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2137a-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="2137a-126">Namespace</span></span><br/> | <span data-ttu-id="2137a-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2137a-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2137a-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="2137a-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2137a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2137a-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2137a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2137a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2137a-131">**AxWindowsMediaPlayer. playstate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2137a-131">**AxWindowsMediaPlayer.playState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2137a-132">**Iwmpcdrom-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2137a-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2137a-133">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2137a-133">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2137a-134">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2137a-134">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





