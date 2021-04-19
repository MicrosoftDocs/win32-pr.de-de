---
description: Einer der Hauptzwecke des Zugriffs auf eine Auflistung besteht darin, ein Element aus der Auflistung zu entfernen. Sie können ein Element aus einer Sammlung entfernen, indem Sie die Methode "Swap. Remove" aufrufen. Diese Methode ist für "errbewbjectset" oder "errbemmethodset" nicht verfügbar.
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: Entfernen eines einzelnen Elements aus einer WMI-Sammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dabeb3ff2e7e70cf6fe25f1ddfb0b14032119d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356625"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a><span data-ttu-id="9b376-105">Entfernen eines einzelnen Elements aus einer WMI-Sammlung</span><span class="sxs-lookup"><span data-stu-id="9b376-105">Removing a Single Item from a WMI Collection</span></span>

<span data-ttu-id="9b376-106">Einer der Hauptzwecke des Zugriffs auf eine Auflistung besteht darin, ein Element aus der Auflistung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9b376-106">One of the main purposes of accessing a collection is to remove an item from the collection.</span></span> <span data-ttu-id="9b376-107">Sie können ein Element aus einer Sammlung entfernen, indem Sie die Methode " [**Swap. Remove**](swbempropertyset-remove.md) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9b376-107">You can remove an item from a collection with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="9b376-108">Diese Methode ist für " [**errbewbjectset**](swbemobjectset.md) " oder " [**errbemmethodset**](swbemmethodset.md)" nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b376-108">This method is not available for [**SWbemObjectSet**](swbemobjectset.md) or [**SWbemMethodSet**](swbemmethodset.md).</span></span>

<span data-ttu-id="9b376-109">Elemente werden nach dem Namen aus dem Austausch von " [**Swap PropertySet**](swbempropertyset.md)", " [**Swap-set**](swbemqualifierset.md)" und " [**Swap namedvalueset**](swbemnamedvalueset.md)" entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b376-109">Items are removed by name from [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md), and [**SWbemNamedValueSet**](swbemnamedvalueset.md).</span></span> <span data-ttu-id="9b376-110">Allerdings werden Elemente in " [**taubemaktualisierungs**](swbemrefresher.md) " durch einen Index entfernt und von der Konstanten, die den Berechtigungs Namen darstellt, von " [**taubemprivilegeset**](swbemprivilegeset.md) " entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b376-110">However, items in [**SWbemRefresher**](swbemrefresher.md) are removed by index and from [**SWbemPrivilegeSet**](swbemprivilegeset.md) by the constant that represents the privilege name.</span></span>

<span data-ttu-id="9b376-111">**So entfernen Sie ein Element aus einer Sammlung**</span><span class="sxs-lookup"><span data-stu-id="9b376-111">**To remove an item from a collection**</span></span>

-   <span data-ttu-id="9b376-112">Im folgenden Codebeispiel wird veranschaulicht, wie das Element mit einem Aufrufen der Methode " [**Swap. Remove**](swbempropertyset-remove.md) " entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9b376-112">The following code example shows how to remove the item with a call to the [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) method.</span></span>

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    <span data-ttu-id="9b376-113">Im folgenden Beispiel wird eine neue Klasse mit dem Namen "newclass" im Stamm \\ -Standard Namespace erstellt und drei Eigenschaften hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9b376-113">The following example creates a new class named "NewClass" in the root\\default namespace and adds three properties to it.</span></span> <span data-ttu-id="9b376-114">Das Skript verwendet dann den Code aus dem vorherigen Beispiel, um die zweite Eigenschaft zu löschen.</span><span class="sxs-lookup"><span data-stu-id="9b376-114">The script then uses the code from the previous example to delete the second property.</span></span>

    ```VB
    ' Obtain an empty class and name it
    Const WBEM_CIMTYPE_STRING = 8
    Set objSWbemService = GetObject("winmgmts:root\default")
    Set objClass = objSWbemService.get()
    Wscript.Echo "Creating class NewClass"
    objClass.Path_.Class = "NewClass"

    ' Add three properties 
    For i = 1 to 3
        objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
    Next
    Getprops()

    ' Remove the Prop2 property
    objClass.Properties_.Remove "Prop2"
    Wscript.Echo "Second property removed "
    Getprops()

    ' Write the changes to the class back
    objClass.Put_

    Sub Getprops()
        Wscript.Echo "Number of Properties = " _
            & objClass.Properties_.Count
        For Each prop in objClass.Properties_
            Wscript.Echo prop.name
        Next
    End Sub
    ```

    

<span data-ttu-id="9b376-115">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md), [zugreifen auf eine](accessing-a-collection.md)Auflistung und [Entfernen mehrerer Elemente aus einer](removing-multiple-items-from-a-collection.md)Auflistung.</span><span class="sxs-lookup"><span data-stu-id="9b376-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing Multiple Items from a Collection](removing-multiple-items-from-a-collection.md).</span></span>

 

 



