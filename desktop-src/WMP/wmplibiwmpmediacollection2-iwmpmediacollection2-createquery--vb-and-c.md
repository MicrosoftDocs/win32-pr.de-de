---
title: IWMPMediaCollection2-Methode "kreatequery"
description: Die Methode "Methode" gibt eine iwmpquery-Schnittstelle zurück, die eine neue Abfrage darstellt.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- Windows Media Player der Methode "kreatequery"
- Methode "winatequery" Windows Media Player, IWMPMediaCollection2 Interface
- IWMPMediaCollection2 Interface, Windows Media Player, Methode "kreatequery"
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318b27a20ba801e1fbed58ff79c5bed7841f8c29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352153"
---
# <a name="iwmpmediacollection2createquery-method"></a><span data-ttu-id="21c97-106">IWMPMediaCollection2:: kreatequery-Methode</span><span class="sxs-lookup"><span data-stu-id="21c97-106">IWMPMediaCollection2::createQuery method</span></span>

<span data-ttu-id="21c97-107">Die- `createQuery` Methode gibt eine **iwmpquery** -Schnittstelle zurück, die eine neue Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="21c97-107">The `createQuery` method returns an **IWMPQuery** interface that represents a new query.</span></span>

## <a name="syntax"></a><span data-ttu-id="21c97-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="21c97-108">Syntax</span></span>


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a><span data-ttu-id="21c97-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="21c97-109">Parameters</span></span>

<span data-ttu-id="21c97-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="21c97-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21c97-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21c97-111">Return value</span></span>

<span data-ttu-id="21c97-112">Eine **WMPLib. iwmpquery** -Schnittstelle, die eine neue, leere Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="21c97-112">A **WMPLib.IWMPQuery** interface that represents a new, empty query.</span></span>

## <a name="remarks"></a><span data-ttu-id="21c97-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21c97-113">Remarks</span></span>

<span data-ttu-id="21c97-114">Das Erstellen einer neuen Abfrage ist der erste Schritt, um eine Verbund Abfrage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="21c97-114">Creating a new query is the first step toward creating a compound query.</span></span>

## <a name="examples"></a><span data-ttu-id="21c97-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21c97-115">Examples</span></span>

<span data-ttu-id="21c97-116">Im folgenden Beispiel `createQuery` wird verwendet, um eine **iwmpquery** -Schnittstelle zu erhalten, die mit NULL initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="21c97-116">The following example uses `createQuery` to get an **IWMPQuery** interface that is initialized to null.</span></span> <span data-ttu-id="21c97-117">Da dieser Abfrage keine Bedingungen hinzugefügt werden, gibt die Methode eine Zeichen folgen Auflistung zurück, die alle Medienelemente des angegebenen Medientyps enthält, wenn Sie als Argument in der **getstringcollectionbyquery** -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21c97-117">Because this query has no conditions added to it, when it is used as an argument in the **getStringCollectionByQuery** method, the method will return a string collection that contains all of the media items of the specified media type.</span></span> <span data-ttu-id="21c97-118">Die Zeichen folgen Sammlung wird dann in einem Listenfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="21c97-118">The string collection is then displayed in a list box.</span></span>


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="21c97-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21c97-119">Requirements</span></span>



| <span data-ttu-id="21c97-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21c97-120">Requirement</span></span> | <span data-ttu-id="21c97-121">Wert</span><span class="sxs-lookup"><span data-stu-id="21c97-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21c97-122">Version</span><span class="sxs-lookup"><span data-stu-id="21c97-122">Version</span></span><br/>   | <span data-ttu-id="21c97-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="21c97-123">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="21c97-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="21c97-124">Namespace</span></span><br/> | <span data-ttu-id="21c97-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="21c97-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="21c97-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="21c97-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="21c97-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="21c97-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21c97-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21c97-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21c97-129">**IWMPMediaCollection2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="21c97-129">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="21c97-130">**Iwmpquery-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="21c97-130">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





