---
title: Iwmpmedia markercount (Eigenschaft)
description: Die markercount-Eigenschaft ruft die Anzahl der Marker im Medien Element ab.
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- markercount-Eigenschaften Fenster Media Player
- markercount-Eigenschaft, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, markercount (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad591d8be66dcd20bc5e59d206a637d9b1181f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358744"
---
# <a name="iwmpmediamarkercount-property"></a><span data-ttu-id="e7054-106">Iwmpmedia:: markercount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e7054-106">IWMPMedia::markerCount property</span></span>

<span data-ttu-id="e7054-107">Die **markercount** -Eigenschaft ruft die Anzahl der Marker im Medien Element ab.</span><span class="sxs-lookup"><span data-stu-id="e7054-107">The **markerCount** property gets the number of markers in the media item.</span></span>

<span data-ttu-id="e7054-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e7054-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7054-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7054-109">Syntax</span></span>


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e7054-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e7054-110">Property value</span></span>

<span data-ttu-id="e7054-111">Ein **System. Int32** -Wert, der die markeranzahl ist.</span><span class="sxs-lookup"><span data-stu-id="e7054-111">A **System.Int32** that is the marker count.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7054-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7054-112">Remarks</span></span>

<span data-ttu-id="e7054-113">Diese Eigenschaft gibt 0 (null) zurück, wenn eine Datei keine Marker enthält, oder wenn das Medien Element nicht mit dem in AxWindowsMediaPlayer. currentMedia angegebenen Zeichen identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e7054-113">This property returns zero if a file has no markers, or if the media item is not the same as the one specified in AxWindowsMediaPlayer.currentMedia.</span></span>

<span data-ttu-id="e7054-114">Markernummern beginnen bei 1.</span><span class="sxs-lookup"><span data-stu-id="e7054-114">Marker numbers start at 1.</span></span>

<span data-ttu-id="e7054-115">Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="e7054-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="e7054-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e7054-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e7054-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7054-117">Examples</span></span>

<span data-ttu-id="e7054-118">Im folgenden Beispiel wird **markercount** verwendet, um die Anzahl der Marker im aktuellen Medien Element abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e7054-118">The following example uses **markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="e7054-119">Dieser Wert wird dann als obere Grenze für eine Schleifen Struktur verwendet, die die markerliste durchläuft, um die einzelnen Markernamen abzurufen und in einem mehrzeiligen Textfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e7054-119">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name and display it in a multi-line text box.</span></span> <span data-ttu-id="e7054-120">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e7054-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
```





## <a name="requirements"></a><span data-ttu-id="e7054-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7054-121">Requirements</span></span>



| <span data-ttu-id="e7054-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7054-122">Requirement</span></span> | <span data-ttu-id="e7054-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e7054-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7054-124">Version</span><span class="sxs-lookup"><span data-stu-id="e7054-124">Version</span></span><br/>   | <span data-ttu-id="e7054-125">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="e7054-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e7054-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7054-126">Namespace</span></span><br/> | <span data-ttu-id="e7054-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e7054-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e7054-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="e7054-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e7054-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e7054-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7054-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7054-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7054-131">**AxWindowsMediaPlayer. currentMedia (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7054-131">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7054-132">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7054-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





