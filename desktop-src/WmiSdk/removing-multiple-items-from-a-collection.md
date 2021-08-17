---
description: Wenn Sie versuchen, mehr als ein Element in einer Sammlung zu entfernen, werden Sie möglicherweise feststellen, dass einige Elemente nicht entfernt werden.
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: Entfernen mehrerer Elemente aus einer WMI-Sammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17795378f5215977e5e7c2d0afd745c5d02fe6b294d062fcdbcf82f7ccc15351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992440"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a>Entfernen mehrerer Elemente aus einer WMI-Sammlung

Wenn Sie versuchen, mehr als ein Element in einer Sammlung zu entfernen, werden Sie möglicherweise feststellen, dass einige Elemente nicht entfernt werden. Sie können beim Entfernen von Elementen keine Auflistung iterieren, da beim Entfernen eines Elements aus einer Auflistung der Auflistungszeiger auf das nächste Element verschoben wird. Beispielsweise führt der Versuch, alle Elemente aus einer Auflistung zu entfernen, zum Entfernen jedes anderen Elements. Dieses Problem wird möglicherweise beim Entfernen von Elementen mit den Methoden [**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md) oder [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) auftreten. Sie können dieses Problem vermeiden, indem Sie eine Schleife durch die Auflistung und die Namen der zu entfernenden Elemente in ein Array setzen. Anschließend können Sie eine Schleife durch das Array und die im Array benannten Elemente löschen. Die Sammlungen, z. B. [**SWbemNamedValueSet,**](swbemnamedvalueset.md) [**SWbemPrivilegeSet**](swbemprivilegeset.md)und [**SWbemRefresher,**](swbemrefresher.md)verfügen auch über eine Methode, die alle Elemente im Aktualisierungscontainer löscht.

Das folgende Skript veranschaulicht, wie mehrere Elemente aus einer Auflistung entfernt werden.


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



Sie können keine Eigenschaften und Qualifizierer in einer Klasseninstanz oder abgeleiteten Klasse entfernen, die über geerbte Eigenschaften verfügt. Ein solcher Löschversuch löst einen Fehler aus, und die Eigenschaft oder der Qualifizierer wird nicht entfernt. Stattdessen setzt WMI die Eigenschaft oder den Qualifizierer auf den Standardwert zurück. Im Fall einer abgeleiteten Klasse mit geerbten Eigenschaften setzt WMI die geerbte Eigenschaft auf den Standardwert der Eigenschaft in der übergeordneten Klasse zurück.

Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen,](manipulating-class-and-instance-information.md)Zugreifen auf eine [Auflistung](accessing-a-collection.md)und Entfernen eines einzelnen Elements aus [einer Auflistung.](removing-a-single-item-from-a-collection.md)

 

 



