---
description: Ein InParameters-Objekt enthält die Parameterliste zum Aufrufen von Anbietermethoden, wenn ein ExecMethod-Aufruftyp verwendet wird.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Erstellen von InParameters-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc13a51687954331a050337fe785bab29b23ee9c72785ffde78d4f8a8e0d198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131582"
---
# <a name="constructing-inparameters-objects"></a>Erstellen von InParameters-Objekten

Ein [**InParameters-Objekt**](swbemmethod-inparameters.md) enthält die Parameterliste zum Aufrufen von Anbietermethoden, wenn ein **ExecMethod-Aufruftyp** verwendet wird. Die [**SWbemObject.ExecMethod, \_**](swbemobject-execmethod-.md) [**SWbemObject.Exe\_ cMethodAsync,**](swbemobject-execmethodasync-.md)SWbemServices.Exe [**cMethod**](swbemservices-execmethod.md)undSWbemServices.Exe [**cMethodAsync**](swbemservices-execmethodasync.md) erfordern alle ein **InParameters-Objekt.**

Im folgenden Verfahren wird beschrieben, wie ein [**InParameters-Objekt erstellt**](swbemmethod-inparameters.md) wird.

**So erstellen Sie *den objwbemInParams-Parameter***

1.  Verbinden WMI.
2.  Abrufen der Definition der WMI-Klasse, die die Methode definiert, die Sie ausführen möchten.
3.  Abrufen eines [**InParameters-Objekts,**](swbemmethod-inparameters.md) das spezifisch für die WMI-Klassenmethode ist, die Sie ausführen möchten.

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  Legen Sie die Eigenschaften der Instanz auf die entsprechenden Werte fest. Achten Sie darauf, den Schlüsseleigenschaften in der WMI-Klasse Werte zu geben, die die Methode enthalten, die Sie ausführen möchten.

    Wenn Sie beispielsweise einen Eingabeparameter namens myinputparam auf den Wert "abc" in einer Instanz von [**InParameters**](swbemmethod-inparameters.md) mit dem Namen "INST" festlegen möchten, sieht der Code wie hier aus.

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  Führen Sie die -Methode aus, und erhalten Sie den Rückgabestatus der Methode, die Sie ausführen.

Das folgende Codebeispiel veranschaulicht das Einrichten des [**InParameters-Objekts**](swbemmethod-inparameters.md) zum Erstellen eines neuen WMI-Objekts, das eine Freigabe darstellt. Weitere Informationen zum [**OutParameters-Objekt**](swbemmethod-outparameters.md) finden Sie unter [Parsing OutParameters Objects](parsing-outparameters-objects.md). In diesem Beispiel wird ein erfolgreicher Rückgabewert (0) zurückgegeben, wenn sich ein Ordner mit dem Namen "Share" am Speicherort "C:/Share" befindet. In diesem Beispiel kann dieser Ordner für andere Benutzer freigegeben werden.


```VB
' Connect to WMI.
Set objServices = GetObject("winmgmts:root\cimv2")

' Obtain the definition of the WMI class that defines
' the method you want to execute.
Set objShare = objServices.Get("Win32_Share")

' Obtain an InParameters object specific
' to the WMI class method you want to execute.
Set objInParam = objShare.Methods_("Create"). _
    inParameters.SpawnInstance_()

' Set the properties of the instance to whatever
' values are appropriate.
objInParam.Properties_.Item("Access") = objSecDescriptor
objInParam.Properties_.Item("Description") = _
    "New share created by WMI script"
objInParam.Properties_.Item("Name") = "share"
objInParam.Properties_.Item("Path") = "C:\share"
objInParam.Properties_.Item("Type") = 0
'optional - default is 'max allowed'
objInParam.Properties_.Item("MaximumAllowed") = 100
'optional - default is no password
objInParam.Properties_.Item("Password") = "Password"

' Execute the method and obtain the return status. 
' The OutParameters object in objOutParams
' is created by the provider. 
Set objOutParams = objShare.ExecMethod_("Create", objInParam)    
wscript.echo objOutParams.ReturnValue
```



 

 



