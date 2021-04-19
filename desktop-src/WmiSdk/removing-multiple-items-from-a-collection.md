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
# <a name="removing-multiple-items-from-a-wmi-collection"></a>Entfernen mehrerer Elemente aus einer WMI-Sammlung

Wenn Sie versuchen, mehr als ein Element in einer Sammlung zu entfernen, werden Sie möglicherweise feststellen, dass einige Elemente nicht entfernt werden. Beim Entfernen von Elementen ist es nicht möglich, eine Auflistung zu durchlaufen, denn wenn Sie ein Element aus einer Auflistung entfernen, wird der Auflistungs Zeiger auf das nächste Element verschoben. Beispielsweise führt der Versuch, alle Elemente aus einer Sammlung zu entfernen, dazu, dass jedes andere Element entfernt wird. Dieses Problem wird möglicherweise angezeigt, wenn Sie Elemente mit der Methode " [**Swap. Remove**](swbemqualifierset-remove.md) " oder " [**gobempropertyset. Remove**](swbempropertyset-remove.md) " entfernen. Sie können dieses Problem vermeiden, indem Sie die Auflistung durchlaufen und die Namen der zu entfernenden Elemente in einem Array ablegen. Anschließend können Sie das Array durchlaufen und die im Array benannten Elemente löschen. Die Auflistungen, wie z. b. " [**Swap namedvalueset**](swbemnamedvalueset.md)", " [**taubemprivilegeset**](swbemprivilegeset.md)" und " [**Swap**](swbemrefresher.md)Update", verfügen ebenfalls über eine Methode, mit der alle Elemente im Aktualisierungs Container gelöscht werden.

Das folgende Skript veranschaulicht, wie mehrere Elemente aus einer Sammlung entfernt werden.


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



Eigenschaften und Qualifizierer können nicht in einer Klasseninstanz oder abgeleiteten Klasse entfernt werden, die Eigenschaften geerbt hat. Bei einem solchen Löschversuch wird ein Fehler ausgelöst, und die Eigenschaft oder der Qualifizierer wird nicht entfernt. Stattdessen setzt WMI die Eigenschaft oder den Qualifizierer auf den Standardwert zurück. Bei einer abgeleiteten Klasse mit geerbten Eigenschaften setzt WMI die geerbte Eigenschaft auf den Standardwert der Eigenschaft in der übergeordneten Klasse zurück.

Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md), [zugreifen auf eine](accessing-a-collection.md)Auflistung und [Entfernen eines einzelnen Elements aus einer](removing-a-single-item-from-a-collection.md)Auflistung.

 

 



