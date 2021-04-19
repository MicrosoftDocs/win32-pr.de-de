---
description: Wenn Sie versuchen, mehr als ein Element in einer Sammlung zu entfernen, werden Sie möglicherweise feststellen, dass einige Elemente nicht entfernt werden.
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: Entfernen mehrerer Elemente aus einer WMI-Sammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c44203f3279163a1de595cac8a00270dccd31c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359554"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a><span data-ttu-id="e535c-103">Entfernen mehrerer Elemente aus einer WMI-Sammlung</span><span class="sxs-lookup"><span data-stu-id="e535c-103">Removing Multiple Items from a WMI Collection</span></span>

<span data-ttu-id="e535c-104">Wenn Sie versuchen, mehr als ein Element in einer Sammlung zu entfernen, werden Sie möglicherweise feststellen, dass einige Elemente nicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e535c-104">If you attempt to remove more than one item in a collection, you may find that some items are not removed.</span></span> <span data-ttu-id="e535c-105">Beim Entfernen von Elementen ist es nicht möglich, eine Auflistung zu durchlaufen, denn wenn Sie ein Element aus einer Auflistung entfernen, wird der Auflistungs Zeiger auf das nächste Element verschoben.</span><span class="sxs-lookup"><span data-stu-id="e535c-105">You cannot iterate a collection while removing items, because when you remove an element from a collection, the collection pointer is moved on to the next element.</span></span> <span data-ttu-id="e535c-106">Beispielsweise führt der Versuch, alle Elemente aus einer Sammlung zu entfernen, dazu, dass jedes andere Element entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="e535c-106">For example, an attempt to remove all of the items from a collection results in the removal of every other item.</span></span> <span data-ttu-id="e535c-107">Dieses Problem wird möglicherweise angezeigt, wenn Sie Elemente mit der Methode " [**Swap. Remove**](swbemqualifierset-remove.md) " oder " [**gobempropertyset. Remove**](swbempropertyset-remove.md) " entfernen.</span><span class="sxs-lookup"><span data-stu-id="e535c-107">You may see this problem when you are removing items with the [**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md) or [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) methods.</span></span> <span data-ttu-id="e535c-108">Sie können dieses Problem vermeiden, indem Sie die Auflistung durchlaufen und die Namen der zu entfernenden Elemente in einem Array ablegen.</span><span class="sxs-lookup"><span data-stu-id="e535c-108">You can avoid this problem by looping through the collection and putting the names of the items to remove in an array.</span></span> <span data-ttu-id="e535c-109">Anschließend können Sie das Array durchlaufen und die im Array benannten Elemente löschen.</span><span class="sxs-lookup"><span data-stu-id="e535c-109">You then can loop through the array and delete the items named in the array.</span></span> <span data-ttu-id="e535c-110">Die Auflistungen, wie z. b. " [**Swap namedvalueset**](swbemnamedvalueset.md)", " [**taubemprivilegeset**](swbemprivilegeset.md)" und " [**Swap**](swbemrefresher.md)Update", verfügen ebenfalls über eine Methode, mit der alle Elemente im Aktualisierungs Container gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e535c-110">The collections, such as [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), and [**SWbemRefresher**](swbemrefresher.md), also have a method that deletes all items in the refresher container.</span></span>

<span data-ttu-id="e535c-111">Das folgende Skript veranschaulicht, wie mehrere Elemente aus einer Sammlung entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e535c-111">The following script illustrates how to remove several items from a collection.</span></span>


```VB
Const WBEM_CIMTYPE_STRING = 8    ' Value for string data type
Dim names()
Redim names (0)
set objSWbemService = GetObject("winmgmts:root\default")
set objClass = ObjSWbemService.Get()

Wscript.Echo "Creating class NewClass"
objClass.Path_.Class = "NewClass"
For i = 1 to 5
    objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
Next
objClass.Put_
Getprops()

' Get all the property names in an array
For Each oprop in objClass.properties_
    Redim Preserve names(Ubound(names)+1)
    names(Ubound(names)-1) = oprop.name
Next
Wscript.Echo "Remove first 3 properties using array of names:"

For i = Lbound(names) to Ubound(names)-1
    If (i < 3) Then
       Wscript.Echo "Removing " & names(i)
       objClass.Properties_.Remove names(i)
    End If
Next

objClass.Put_
Wscript.Echo "Result:"
Getprops()

Sub Getprops()
    Wscript.Echo "Number of properties = " _
        & objClass.Properties_.Count
    For Each oprop in objClass.Properties_
        Wscript.Echo oprop.name
    Next
End Sub
```



Eigenschaften und Qualifizierer können nicht in einer Klasseninstanz oder abgeleiteten Klasse entfernt werden, die Eigenschaften geerbt hat. Bei einem solchen Löschversuch wird ein Fehler ausgelöst, und die Eigenschaft oder der Qualifizierer wird nicht entfernt. Stattdessen setzt WMI die Eigenschaft oder den Qualifizierer auf den Standardwert zurück. <span data-ttu-id="e535c-114">Bei einer abgeleiteten Klasse mit geerbten Eigenschaften setzt WMI die geerbte Eigenschaft auf den Standardwert der Eigenschaft in der übergeordneten Klasse zurück.</span><span class="sxs-lookup"><span data-stu-id="e535c-114">In the case of a derived class with inherited properties, WMI resets the inherited property to the default value of the property in the parent class.</span></span>

<span data-ttu-id="e535c-115">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md), [zugreifen auf eine](accessing-a-collection.md)Auflistung und [Entfernen eines einzelnen Elements aus einer](removing-a-single-item-from-a-collection.md)Auflistung.</span><span class="sxs-lookup"><span data-stu-id="e535c-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing a Single Item from a Collection](removing-a-single-item-from-a-collection.md).</span></span>

 

 



