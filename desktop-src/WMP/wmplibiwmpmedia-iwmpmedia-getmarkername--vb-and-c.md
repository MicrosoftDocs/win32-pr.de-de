---
title: Iwmpmedia getmarkername-Methode
description: Die getmarkername-Methode gibt den Namen des Markers am angegebenen Index zurück.
ms.assetid: 77f893cf-1669-41e3-9f62-8a1081e37add
keywords:
- getmarkername-Methode, Windows Media Player
- getmarkername-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, getmarkername-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ba6a7bb640a397cce9c7dfd22b5f9b6203c47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370312"
---
# <a name="iwmpmediagetmarkername-method"></a><span data-ttu-id="6b3f8-106">Iwmpmedia:: getmarkername-Methode</span><span class="sxs-lookup"><span data-stu-id="6b3f8-106">IWMPMedia::getMarkerName method</span></span>

<span data-ttu-id="6b3f8-107">Die **getmarkername** -Methode gibt den Namen des Markers am angegebenen Index zurück.</span><span class="sxs-lookup"><span data-stu-id="6b3f8-107">The **getMarkerName** method returns the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b3f8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b3f8-108">Syntax</span></span>


```CSharp
public System.String getMarkerName(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerName( _
  ByVal MarkerNum As System.Int32 _
) As System.String
Implements IWMPMedia.getMarkerName
```





## <a name="parameters"></a><span data-ttu-id="6b3f8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b3f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b3f8-110">*Markernum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b3f8-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b3f8-111">Ein **System. Int32** -Wert, der der MarkerIndex ist.</span><span class="sxs-lookup"><span data-stu-id="6b3f8-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b3f8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b3f8-112">Return value</span></span>

<span data-ttu-id="6b3f8-113">Ein **System. String** -Wert, der der markerName ist.</span><span class="sxs-lookup"><span data-stu-id="6b3f8-113">A **System.String** that is the marker name.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b3f8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b3f8-114">Remarks</span></span>

<span data-ttu-id="6b3f8-115">Diese Methode gibt **null** zurück, wenn der angegebene Marker nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6b3f8-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="6b3f8-116">Einige Medienelemente enthalten keine Marker.</span><span class="sxs-lookup"><span data-stu-id="6b3f8-116">Some media items do not contain markers.</span></span> <span data-ttu-id="6b3f8-117">Verwenden Sie **markercount** , um herauszufinden, wie viele Marker im aktuellen Medien Element sind.</span><span class="sxs-lookup"><span data-stu-id="6b3f8-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="6b3f8-118">Markerindexnummern beginnen bei 1.</span><span class="sxs-lookup"><span data-stu-id="6b3f8-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="6b3f8-119">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="6b3f8-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="6b3f8-120">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6b3f8-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6b3f8-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b3f8-121">Examples</span></span>

<span data-ttu-id="6b3f8-122">Im folgenden Codebeispiel wird **getmarkername** verwendet, um ein mehr zeitiges Textfeld mit den Namen der Marker im aktuellen Medien Element auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="6b3f8-122">The following code example uses **getMarkerName** to fill a multi-line text box with the names of the markers in the current media item.</span></span> <span data-ttu-id="6b3f8-123">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6b3f8-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker names
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markers[i] = player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerNames.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mCount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker names
Dim markers(mCount) As String

&#39; Verify that at least one marker exists in the current media.
If (mCount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mCount

        &#39; Store the marker name in the array.
        markers(i) = player.currentMedia.getMarkerName(i)

    Next i

End If

&#39; Display the marker names in the text box.
markerNames.Lines = markers
```





## <a name="requirements"></a><span data-ttu-id="6b3f8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b3f8-124">Requirements</span></span>



| <span data-ttu-id="6b3f8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b3f8-125">Requirement</span></span> | <span data-ttu-id="6b3f8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6b3f8-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b3f8-127">Version</span><span class="sxs-lookup"><span data-stu-id="6b3f8-127">Version</span></span><br/>   | <span data-ttu-id="6b3f8-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="6b3f8-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6b3f8-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b3f8-129">Namespace</span></span><br/> | <span data-ttu-id="6b3f8-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6b3f8-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6b3f8-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="6b3f8-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6b3f8-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6b3f8-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b3f8-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b3f8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b3f8-134">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6b3f8-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6b3f8-135">**Iwmpmedia. markercount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6b3f8-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





