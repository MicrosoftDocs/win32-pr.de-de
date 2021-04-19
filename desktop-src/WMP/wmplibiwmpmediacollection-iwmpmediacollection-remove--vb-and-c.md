---
title: Iwmpmediacollection-Methode entfernen
description: Die Remove-Methode entfernt ein angegebenes Element aus der Medien Auflistung.
ms.assetid: 2ed45159-0a92-4353-8bf1-1d20de404bf7
keywords:
- Methode "Windows Media Player entfernen"
- Remove-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection-Schnittstelle, Windows Media Player, Methode entfernen
topic_type:
- apiref
api_name:
- IWMPMediaCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d341f8974255dab5e3cdce356a9b221eddff193c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374017"
---
# <a name="iwmpmediacollectionremove-method"></a><span data-ttu-id="05e34-106">Iwmpmediacollection:: Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="05e34-106">IWMPMediaCollection::remove method</span></span>

<span data-ttu-id="05e34-107">Die- `remove` Methode entfernt ein angegebenes Element aus der Medien Auflistung.</span><span class="sxs-lookup"><span data-stu-id="05e34-107">The `remove` method removes a specified item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="05e34-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="05e34-108">Syntax</span></span>


```CSharp
public void remove(
  IWMPMedia pItem,
  System.Boolean varfDeleteFile
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPMedia, _
  ByVal varfDeleteFile As System.Boolean _
)
Implements IWMPMediaCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="05e34-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="05e34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05e34-110">*pitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05e34-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05e34-111">Eine **WMPLib. iwmpmedia** -Schnittstelle, die das zu entfernende Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="05e34-111">A **WMPLib.IWMPMedia** interface that identifies the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="05e34-112">*varbdeletefile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05e34-112">*varfDeleteFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05e34-113">Ein **System. Boolean** -Wert, der angibt, ob die-Methode das angegebene Element aus der Bibliothek entfernen soll.</span><span class="sxs-lookup"><span data-stu-id="05e34-113">A **System.Boolean** value that specifies whether the method should remove the specified item from the library.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05e34-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05e34-114">Return value</span></span>

<span data-ttu-id="05e34-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="05e34-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05e34-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05e34-116">Remarks</span></span>

<span data-ttu-id="05e34-117">Diese Methode löscht ein Element aus der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="05e34-117">This method deletes an item from the library.</span></span> <span data-ttu-id="05e34-118">Mit dieser Methode werden keine Dateien auf dem Computer des Benutzers gelöscht.</span><span class="sxs-lookup"><span data-stu-id="05e34-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="05e34-119">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="05e34-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="05e34-120">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="05e34-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="05e34-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05e34-121">Examples</span></span>

<span data-ttu-id="05e34-122">Im folgenden Beispiel wird nach dem auffordern des Benutzers das erste Medien Element in der Medien Auflistung dauerhaft mithilfe von gelöscht `remove` .</span><span class="sxs-lookup"><span data-stu-id="05e34-122">The following example, after prompting the user, permanently deletes the first media item in the media collection by using `remove`.</span></span> <span data-ttu-id="05e34-123">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="05e34-123">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first item from the media collection. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Store the name of the retrieved media item.
string mediaName = media.name;

// Prepare a message, a caption and buttons for the user prompt.
string message = ("OK to permanently delete " + mediaName + "?");
string caption = "Confirm deletion";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.OKCancel;

// Prompt the user for permission to delete the object.
System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

// Check the user response.
if (result == System.Windows.Forms.DialogResult.OK)
{
    // Permanently delete the item.
    player.mediaCollection.remove(media, true);

    // Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show("Deleted item " + mediaName);
}
```


```VB

' Get an interface to the first item from the media collection. 
Dim media As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Store the name of the retrieved media item.
Dim mediaName As String = media.name

&#39; Prepare a message, a caption and buttons for the user prompt.
Dim message As String = (&quot;OK to permanently delete &quot; + mediaName + &quot;?&quot;)
Dim caption As String = &quot;Confirm deletion&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.OKCancel

&#39; Prompt the user for permission to delete the object.
Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

&#39; Check the user response.
If (result = System.Windows.Forms.DialogResult.OK) Then

    &#39; Permanently delete the item.
    player.mediaCollection.remove(media, True)

    &#39; Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show(&quot;Deleted item &quot; + mediaName)

End If
```





## <a name="requirements"></a><span data-ttu-id="05e34-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05e34-124">Requirements</span></span>



| <span data-ttu-id="05e34-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05e34-125">Requirement</span></span> | <span data-ttu-id="05e34-126">Wert</span><span class="sxs-lookup"><span data-stu-id="05e34-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05e34-127">Version</span><span class="sxs-lookup"><span data-stu-id="05e34-127">Version</span></span><br/>   | <span data-ttu-id="05e34-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="05e34-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="05e34-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="05e34-129">Namespace</span></span><br/> | <span data-ttu-id="05e34-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="05e34-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="05e34-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="05e34-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="05e34-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="05e34-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05e34-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05e34-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05e34-134">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="05e34-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="05e34-135">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="05e34-135">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="05e34-136">**Iwmpmediacollection. Add (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="05e34-136">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> </dl>

 

 





