---
description: Einer der Hauptzwecke für den Zugriff auf eine Auflistung ist das Entfernen eines Elements aus der Auflistung. Sie können ein Element mit einem Aufruf der SWbemPropertySet.Remove-Methode aus einer Auflistung entfernen. Diese Methode ist für SWbemObjectSet oder SWbemMethodSet nicht verfügbar.
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: Entfernen eines einzelnen Elements aus einer WMI-Sammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50364173aff9f28362878e84d5f3ddb496e430521dc5b1bb92bbc11e7e6b528c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995900"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a>Entfernen eines einzelnen Elements aus einer WMI-Sammlung

Einer der Hauptzwecke für den Zugriff auf eine Auflistung ist das Entfernen eines Elements aus der Auflistung. Sie können ein Element mit einem Aufruf der [**SWbemPropertySet.Remove-Methode**](swbempropertyset-remove.md) aus einer Auflistung entfernen. Diese Methode ist für [**SWbemObjectSet oder**](swbemobjectset.md) [**SWbemMethodSet nicht verfügbar.**](swbemmethodset.md)

Elemente werden nach Namen aus [**SWbemPropertySet,**](swbempropertyset.md) [**SWbemQualifierSet**](swbemqualifierset.md)und [**SWbemNamedValueSet entfernt.**](swbemnamedvalueset.md) Elemente in [**SWbemRefresher**](swbemrefresher.md) werden jedoch nach Index und [**aus SWbemPrivilegeSet**](swbemprivilegeset.md) durch die Konstante entfernt, die den Berechtigungsnamen darstellt.

**So entfernen Sie ein Element aus einer Auflistung**

-   Das folgende Codebeispiel zeigt, wie das Element mit einem Aufruf der [**SWbemPropertySet.Remove-Methode entfernt**](swbempropertyset-remove.md) wird.

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    Im folgenden Beispiel wird eine neue Klasse namens "NewClass" im Stamm-Standardnamespace erstellt und ihr \\ drei Eigenschaften hinzufügt. Das Skript verwendet dann den Code aus dem vorherigen Beispiel, um die zweite Eigenschaft zu löschen.

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

    

Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen,](manipulating-class-and-instance-information.md)Zugreifen auf eine [Auflistung](accessing-a-collection.md)und Entfernen mehrerer Elemente aus [einer Auflistung.](removing-multiple-items-from-a-collection.md)

 

 



