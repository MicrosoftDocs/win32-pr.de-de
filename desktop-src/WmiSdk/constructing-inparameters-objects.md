---
description: Ein InParameters-Objekt enthält die Parameterliste zum Aufrufen von Anbieter Methoden, wenn ein ExecMethod-Aufgabentyp verwendet wird.
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: Erstellen von InParameters-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf9a351caec1ca7af3113bead4078670c88a5f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864035"
---
# <a name="constructing-inparameters-objects"></a>Erstellen von InParameters-Objekten

Ein [**InParameters**](swbemmethod-inparameters.md) -Objekt enthält die Parameterliste zum Aufrufen von Anbieter Methoden, wenn ein **ExecMethod** -Aufgabentyp verwendet wird. Die [**MethodenSWbemObject.Execmethod \_**](swbemobject-execmethod-.md), [**SWbemObject.Execmethodasync \_**](swbemobject-execmethodasync-.md), [**SWbemServices.Execmethod**](swbemservices-execmethod.md)und [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md) erfordern alle ein **InParameters** -Objekt.

Im folgenden Verfahren wird beschrieben, wie ein [**InParameters**](swbemmethod-inparameters.md) -Objekt erstellt wird.

**So erstellen Sie den *objwbeminparameams* -Parameter**

1.  Verbindung mit WMI herstellen.
2.  Rufen Sie die Definition der WMI-Klasse ab, die die Methode definiert, die Sie ausführen möchten.
3.  Rufen Sie ein [**InParameters**](swbemmethod-inparameters.md) -Objekt für die WMI-Klassenmethode ab, die Sie ausführen möchten.

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  Legen Sie die Eigenschaften der-Instanz auf die geeigneten Werte fest. Stellen Sie sicher, dass Sie den Schlüsseleigenschaften in der WMI-Klasse Werte geben, die die auszuführende Methode enthält.

    Wenn Sie z. b. einen Eingabeparameter mit dem Namen myinputparam auf den Wert "ABC" in einer Instanz von [**InParameters**](swbemmethod-inparameters.md) namens "Inst" festlegen möchten, sieht der Code wie folgt aus.

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  Führen Sie die-Methode aus, und rufen Sie den Rückgabestatus der Methode ab, die Sie ausführen.

Das folgende Codebeispiel veranschaulicht das Einrichten des [**InParameters**](swbemmethod-inparameters.md) -Objekts, um ein neues WMI-Objekt zu erstellen, das eine Freigabe darstellt. Weitere Informationen zum [**OutParameters**](swbemmethod-outparameters.md) -Objekt finden Sie unter "Überprüfen von [outparameter-Objekten](parsing-outparameters-objects.md)". In diesem Beispiel wird ein erfolgreicher Rückgabewert (0) zurückgegeben, wenn ein Ordner mit dem Namen "Share" am Speicherort "C:/Share" vorhanden ist. In diesem Beispiel kann dieser Ordner für andere Benutzer freigegeben werden.


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



 

 



