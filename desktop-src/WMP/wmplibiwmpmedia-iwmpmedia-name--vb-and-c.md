---
title: Iwmpmedia Name (Eigenschaft)
description: Die Name-Eigenschaft ruft den Namen des Medien Elements ab oder legt ihn fest.
ms.assetid: d1057871-bccf-4f84-9b1d-74c41a8f7f7c
keywords:
- Name der Eigenschaften Fenster Media Player
- Name-Eigenschaft, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPMedia.name
- IWMPMedia.get_name
- IWMPMedia.put_name
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c526fc9847b06d0f7b6f4ebadf71761fd29a9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367089"
---
# <a name="iwmpmedianame-property"></a><span data-ttu-id="2110d-106">Iwmpmedia:: Name (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2110d-106">IWMPMedia::name property</span></span>

<span data-ttu-id="2110d-107">Die **Name** -Eigenschaft ruft den Namen des Medien Elements ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="2110d-107">The **name** property gets or sets the name of the media item.</span></span>

<span data-ttu-id="2110d-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2110d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2110d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2110d-109">Syntax</span></span>


```CSharp
public System.String name {get; set;}
```


```VB

Public Property name As System.String
```





## <a name="property-value"></a><span data-ttu-id="2110d-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2110d-110">Property value</span></span>

<span data-ttu-id="2110d-111">Ein **System. String** -Wert, der der Name des Medien Elements ist.</span><span class="sxs-lookup"><span data-stu-id="2110d-111">A **System.String** that is the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="2110d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2110d-112">Remarks</span></span>

<span data-ttu-id="2110d-113">Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="2110d-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="2110d-114">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2110d-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2110d-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2110d-115">Examples</span></span>

<span data-ttu-id="2110d-116">Im folgenden Beispiel wird **Name** verwendet, um den Namen des aktuellen Medien Elements zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2110d-116">The following example uses **name** to change the name of the current media item.</span></span> <span data-ttu-id="2110d-117">Ein Textfeld ermöglicht dem Benutzer, einen neuen Namen einzugeben, und der Name wird als Reaktion auf das Click-Ereignis einer Schaltfläche geändert.</span><span class="sxs-lookup"><span data-stu-id="2110d-117">A text box allows the user to enter a new name, and the name is changed in response to the Click event of a button.</span></span> <span data-ttu-id="2110d-118">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2110d-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewName_Click(object sender, System.EventArgs e)
{
    // ...Add code to ensure that the TextBox contains a valid value.

    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Change the name. 
    cm.name = nameText.Text;
}
```


```VB

Public Sub setNewName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewName.Click

    &#39; ...Add code to ensure that the TextBox contains a valid value.

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Change the name. 
    cm.name = nameText.Text

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2110d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2110d-119">Requirements</span></span>



| <span data-ttu-id="2110d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2110d-120">Requirement</span></span> | <span data-ttu-id="2110d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2110d-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2110d-122">Version</span><span class="sxs-lookup"><span data-stu-id="2110d-122">Version</span></span><br/>   | <span data-ttu-id="2110d-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="2110d-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2110d-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2110d-124">Namespace</span></span><br/> | <span data-ttu-id="2110d-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2110d-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2110d-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="2110d-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2110d-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2110d-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2110d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2110d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2110d-129">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2110d-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





