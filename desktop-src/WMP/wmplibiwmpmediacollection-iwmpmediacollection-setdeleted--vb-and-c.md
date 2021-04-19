---
title: "' Iwmpmediacollection ' (SetDeleted-Methode)"
description: Die SetDeleted-Methode verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente". | ' Iwmpmediacollection ' (SetDeleted-Methode)
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- SetDeleted-Methoden Fenster Media Player
- SetDeleted-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection-Schnittstelle, Windows Media Player, SetDeleted-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ccf8cf2d36ab7e4aaf76fdbe5c28582650fcda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370841"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a><span data-ttu-id="7f115-107">Iwmpmediacollection:: SetDeleted-Methode</span><span class="sxs-lookup"><span data-stu-id="7f115-107">IWMPMediaCollection::setDeleted method</span></span>

<span data-ttu-id="7f115-108">Die- `setDeleted` Methode verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente".</span><span class="sxs-lookup"><span data-stu-id="7f115-108">The `setDeleted` method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f115-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f115-109">Syntax</span></span>


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a><span data-ttu-id="7f115-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f115-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f115-111">*pitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f115-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f115-112">Eine **WMPLib. iwmpmedia** -Schnittstelle für das Element, das verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f115-112">A **WMPLib.IWMPMedia** interface for the item to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="7f115-113">*varfisdeleted* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f115-113">*varfIsDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f115-114">Ein **System. Boolean** -Wert, der angibt, ob das Element in den Ordner für gelöschte Elemente verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f115-114">A **System.Boolean** value that specifies whether the item should be moved to the deleted items folder.</span></span> <span data-ttu-id="7f115-115">Dieser Wert muss immer " **true**" sein.</span><span class="sxs-lookup"><span data-stu-id="7f115-115">This value must always be **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f115-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f115-116">Return value</span></span>

<span data-ttu-id="7f115-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7f115-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f115-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f115-118">Remarks</span></span>

<span data-ttu-id="7f115-119">Diese Methode entfernt keine Dateien vom Computer des Benutzers, sondern verschiebt Sie lediglich in den Ordner "Gelöschte Elemente".</span><span class="sxs-lookup"><span data-stu-id="7f115-119">This method does not remove files from the user's computer, it just moves them to the deleted items folder.</span></span>

<span data-ttu-id="7f115-120">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="7f115-120">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="7f115-121">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7f115-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7f115-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f115-122">Examples</span></span>

<span data-ttu-id="7f115-123">Im folgenden Beispiel wird verwendet `setDeleted` , um ein bestimmtes Medien Element in den Ordner "Gelöschte Elemente" zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="7f115-123">The following example uses `setDeleted` to move a particular media item to the deleted items folder.</span></span> <span data-ttu-id="7f115-124">Die **isDeleted** -Methode testet zunächst, ob das Element bereits gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="7f115-124">The **isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="7f115-125">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7f115-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="7f115-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f115-126">Requirements</span></span>



| <span data-ttu-id="7f115-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f115-127">Requirement</span></span> | <span data-ttu-id="7f115-128">Wert</span><span class="sxs-lookup"><span data-stu-id="7f115-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f115-129">Version</span><span class="sxs-lookup"><span data-stu-id="7f115-129">Version</span></span><br/>   | <span data-ttu-id="7f115-130">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="7f115-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7f115-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f115-131">Namespace</span></span><br/> | <span data-ttu-id="7f115-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7f115-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7f115-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="7f115-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7f115-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7f115-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f115-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f115-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f115-136">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="7f115-136">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7f115-137">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="7f115-137">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





