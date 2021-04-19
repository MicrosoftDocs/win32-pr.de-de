---
title: Iwmpmedia GetAttributeName-Methode
description: Die GetAttributeName-Methode gibt den Namen des Attributs zurück, das dem angegebenen Index entspricht.
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- GetAttributeName-Methode, Windows-Media Player
- GetAttributeName-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, GetAttributeName-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb40ef8c0c984258dc11dd00c80807db2f4eb64a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362095"
---
# <a name="iwmpmediagetattributename-method"></a><span data-ttu-id="bc8f1-106">Iwmpmedia:: GetAttributeName-Methode</span><span class="sxs-lookup"><span data-stu-id="bc8f1-106">IWMPMedia::getAttributeName method</span></span>

<span data-ttu-id="bc8f1-107">Die **GetAttributeName** -Methode gibt den Namen des Attributs zurück, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="bc8f1-107">The **getAttributeName** method returns the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8f1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc8f1-108">Syntax</span></span>


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a><span data-ttu-id="bc8f1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc8f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc8f1-110">*Lindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc8f1-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8f1-111">Ein **System. Int32** -Wert, der der Index ist.</span><span class="sxs-lookup"><span data-stu-id="bc8f1-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc8f1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc8f1-112">Return value</span></span>

<span data-ttu-id="bc8f1-113">Ein **System. String** -Wert, der der Attribut Name ist.</span><span class="sxs-lookup"><span data-stu-id="bc8f1-113">A **System.String** that is the attribute name.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc8f1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc8f1-114">Remarks</span></span>

<span data-ttu-id="bc8f1-115">Der zurückgegebene Attribut Name kann in Verbindung mit **getiteminfo** verwendet werden, um den Wert für ein bestimmtes benanntes Attribut abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bc8f1-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="bc8f1-116">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="bc8f1-116">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="bc8f1-117">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="bc8f1-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="bc8f1-118">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="bc8f1-118">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bc8f1-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc8f1-119">Examples</span></span>

<span data-ttu-id="bc8f1-120">Im folgenden Beispiel wird **GetAttributeName** verwendet, um ein mehr zeitiges Textfeld mit dem Index und dem Namen der einzelnen Attribute für das aktuelle Medien Element auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="bc8f1-120">The following example uses **getAttributeName** to fill a multi-line text box with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="bc8f1-121">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bc8f1-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
```





## <a name="requirements"></a><span data-ttu-id="bc8f1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc8f1-122">Requirements</span></span>



| <span data-ttu-id="bc8f1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc8f1-123">Requirement</span></span> | <span data-ttu-id="bc8f1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="bc8f1-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8f1-125">Version</span><span class="sxs-lookup"><span data-stu-id="bc8f1-125">Version</span></span><br/>   | <span data-ttu-id="bc8f1-126">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="bc8f1-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bc8f1-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc8f1-127">Namespace</span></span><br/> | <span data-ttu-id="bc8f1-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="bc8f1-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bc8f1-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="bc8f1-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bc8f1-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bc8f1-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc8f1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc8f1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8f1-132">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="bc8f1-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bc8f1-133">**Iwmpmedia. getiteminfo (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="bc8f1-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





