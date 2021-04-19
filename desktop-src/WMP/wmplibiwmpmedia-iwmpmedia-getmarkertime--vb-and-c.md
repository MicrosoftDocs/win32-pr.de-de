---
title: Iwmpmedia getmarkertime-Methode
description: Die getmarkertime-Methode gibt die Zeit des Markers am angegebenen Index zurück.
ms.assetid: 1c617e3a-0978-479c-a636-b655082232c1
keywords:
- getmarkertime-Methode, Windows-Media Player
- getmarkertime-Methode, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, getmarkertime-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df171977adeee3b597cab1f40469af1d975425c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370800"
---
# <a name="iwmpmediagetmarkertime-method"></a><span data-ttu-id="c1e70-106">Iwmpmedia:: getmarkertime-Methode</span><span class="sxs-lookup"><span data-stu-id="c1e70-106">IWMPMedia::getMarkerTime method</span></span>

<span data-ttu-id="c1e70-107">Die **getmarkertime** -Methode gibt die Zeit des Markers am angegebenen Index zurück.</span><span class="sxs-lookup"><span data-stu-id="c1e70-107">The **getMarkerTime** method returns the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e70-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1e70-108">Syntax</span></span>


```CSharp
public System.Double getMarkerTime(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerTime( _
  ByVal MarkerNum As System.Int32 _
) As System.Double
Implements IWMPMedia.getMarkerTime
```





## <a name="parameters"></a><span data-ttu-id="c1e70-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1e70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e70-110">*Markernum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1e70-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e70-111">Ein **System. Int32** -Wert, der der MarkerIndex ist.</span><span class="sxs-lookup"><span data-stu-id="c1e70-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e70-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1e70-112">Return value</span></span>

<span data-ttu-id="c1e70-113">Ein **System. Double** -Wert, der die Markerzeit ist.</span><span class="sxs-lookup"><span data-stu-id="c1e70-113">A **System.Double** that is the marker time.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e70-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1e70-114">Remarks</span></span>

<span data-ttu-id="c1e70-115">Diese Methode gibt **null** zurück, wenn der angegebene Marker nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c1e70-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="c1e70-116">Einige Medienelemente enthalten keine Marker.</span><span class="sxs-lookup"><span data-stu-id="c1e70-116">Some media items do not contain markers.</span></span> <span data-ttu-id="c1e70-117">Verwenden Sie **markercount** , um herauszufinden, wie viele Marker im aktuellen Medien Element sind.</span><span class="sxs-lookup"><span data-stu-id="c1e70-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="c1e70-118">Markerindexnummern beginnen bei 1.</span><span class="sxs-lookup"><span data-stu-id="c1e70-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="c1e70-119">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="c1e70-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="c1e70-120">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c1e70-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c1e70-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1e70-121">Examples</span></span>

<span data-ttu-id="c1e70-122">Im folgenden Codebeispiel wird **getmarkertime** verwendet, um ein mehrzeilige Textfeld mit der Position der einzelnen Marker auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="c1e70-122">The following code example uses **getMarkerTime** to fill a multi-line text box with the location of each marker.</span></span> <span data-ttu-id="c1e70-123">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c1e70-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker times.
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker information in the array.
        markers[i] = "Marker number " + i + " occurs at ";
        markers[i] += player.currentMedia.getMarkerTime(i).ToString();
        markers[i] += " second(s).";
    }

    // Display the marker times in the text box.
    markerTimes.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker times.
Dim markers(mcount) As String

&#39; Verify that at least one marker exists in the current media.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker information in the array.
        markers(i) = (&quot;Marker number &quot; + i + &quot; occurs at &quot;)
        markers(i) += player.currentMedia.getMarkerTime(i).ToString()
        markers(i) += &quot; second(s).&quot;

    Next i

    &#39; Display the marker times in the text box.
    markerTimes.Lines = markers

End If
```





## <a name="requirements"></a><span data-ttu-id="c1e70-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1e70-124">Requirements</span></span>



| <span data-ttu-id="c1e70-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1e70-125">Requirement</span></span> | <span data-ttu-id="c1e70-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e70-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e70-127">Version</span><span class="sxs-lookup"><span data-stu-id="c1e70-127">Version</span></span><br/>   | <span data-ttu-id="c1e70-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="c1e70-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c1e70-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1e70-129">Namespace</span></span><br/> | <span data-ttu-id="c1e70-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c1e70-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c1e70-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="c1e70-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c1e70-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c1e70-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e70-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1e70-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e70-134">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c1e70-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c1e70-135">**Iwmpmedia. markercount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c1e70-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





